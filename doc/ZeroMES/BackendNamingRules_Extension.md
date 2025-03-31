
# 🧾 Zensoft / ZeroMES 後台開發命名規則補充（二）

## 👉 變數、屬性、方法、常數命名慣例（依 .NET C# 標準與你們架構）

---

## 🟦 1. 變數命名（Local Variables）

| 規則 | 範例 | 備註 |
|------|------|------|
| 使用 camelCase | `isEnabled`, `workOrderId`, `deviceList` | 僅在方法、區域內使用 |
| 使用有意義的語意 | `itemCount`, `retryLimit` | 避免像 `a`, `b`, `temp` 這類模糊命名 |
| 使用縮寫需清楚 | `url`, `dto`, `ipAddress` | 不建議使用不常見簡寫 |

---

## 🟧 2. 屬性命名（Properties）

| 規則 | 範例 | 備註 |
|------|------|------|
| 使用 PascalCase | `WorkOrderId`, `CreatedTime`, `Status` | 每個單字開頭大寫 |
| 為布林值用 Is / Has / Can 開頭 | `IsActive`, `HasError`, `CanExecute` | |
| DTO 屬性命名應清楚對應資料表欄位語意 | `ProductCode`, `LineName`, `OperatorId` | 建議與 DB 命名一致但用 PascalCase |

---

## 🟩 3. 方法命名（Functions / Methods）

| 規則 | 範例 | 說明 |
|------|------|------|
| 使用動詞開頭（Do Something） | `CreateOrder()`, `UpdateStatus()`, `GetItems()` | |
| 回傳 bool 可用 Is / Has | `IsValid()`, `HasPermission()` | |
| 回傳集合可用複數 | `GetUsers()`, `FetchDevices()` | |
| 命名明確傳達功能 | `GenerateLabel()`, `UploadFile()` | 避免 `Process()`, `DoWork()` 模糊命名 |

---

## 🟥 4. 常數與靜態欄位（Constants / static readonly）

| 規則 | 範例 | 備註 |
|------|------|------|
| 常數使用 PascalCase 或 ALL_CAPS | `MaxRetryCount`, `DefaultTimeoutSeconds`, `APP_VERSION` | 團隊可選一種風格統一 |
| 放在 Consts.cs 或 Settings.cs 中 | `ZensoftConsts.AppName` | 方便管理與全域使用 |

---

## 🟨 5. 列舉（Enums）

| 規則 | 範例 | 備註 |
|------|------|------|
| Enum 類別用 PascalCase 單數 | `EquipmentStatus`, `UserRole` | |
| Enum 成員也用 PascalCase | `Idle`, `Running`, `Maintenance` | |
| 避免加前綴，例如不要 `Status_Idle` | 名稱已包含語意不需重複 |

---

## 📌 命名最佳實踐 Tips

- ✅ 命名要反映出用途與意圖，而不是實作細節。
- ✅ 保持命名一致性（用詞統一：是 `Id` 還是 `ID`？是 `Code` 還是 `Number`？）
- ✅ 不建議縮寫整個詞（像 `WkOrd`, `Srvc`），除非是廣為人知的（如 `URL`, `API`）

---

## ✅ 範例整理（綜合範例）

```csharp
public class EquipmentDto
{
    public int Id { get; set; }
    public string Name { get; set; }
    public EquipmentStatus Status { get; set; }
    public DateTime CreatedTime { get; set; }
    public string CreatedBy { get; set; }
}

public interface IEquipmentService
{
    Task<List<EquipmentDto>> GetAllAsync();
    Task<bool> IsNameUniqueAsync(string name);
    Task CreateAsync(EquipmentDto dto);
}
```
