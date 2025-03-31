
# 🧾 Zensoft / ZeroMES 後台開發命名規則

## 🧱 專案與命名空間規則

| 類別 | 命名範例 | 說明 |
|------|----------|------|
| Solution | `Zensoft.sln` | 主解決方案檔 |
| Module Solution | `ZeroMES.sln` | 子模組獨立管理 |
| Namespace Root | `Zensoft.*` / `ZeroMES.*` | 主系統 / MES 模組命名空間前綴 |

---

## 📦 專案資料夾命名規則

| 類型 | 命名範例 | 功能說明 |
|------|----------|----------|
| 核心共用 | `Zensoft.Core` | Entity、介面、常數、驗證邏輯 |
| 基礎建設 | `Zensoft.EFCore`, `Zensoft.Infra` | EF 設定、工具類、快取、時間服務 |
| 共用 Blazor 客戶端工具 | `Zensoft.Infra.Client` | 通用 Dialog、Toast、APIClient |
| API 專案 | `Zensoft.SYS.API`, `ZeroMES.WIP.API` | 每個功能模組對應 API |
| Repository 專案 | `Zensoft.SYS.Repositories` | 定義 + 實作 Repository |
| Service 專案 | `Zensoft.SYS.Services` | 定義 + 實作 Service |
| Blazor 前端 | `Zensoft.Web.Host`, `ZeroMES.WIP.Client` | CRUD、Dashboard 畫面 |
| Event 模組 | `ZeroMES.Events` | WIP/設備/庫存事件邏輯處理 |

---

## 📁 目錄/類別命名慣例

```plaintext
├── Entities/        → Entity 定義
├── Dtos/            → 資料傳輸物件
├── Repositories/    → 介面與實作
├── Services/        → 商業邏輯
├── Controllers/     → API 控制器
├── Pages/           → Blazor UI
├── Extensions/      → 擴充方法
├── Events/          → 事件處理
```

---

## 🧑‍💻 類別命名規則

| 類型 | 命名範例 | 說明 |
|------|----------|------|
| Entity | `WorkOrder`, `Equipment` | 單數名詞，PascalCase |
| DTO | `CreateWorkOrderDto`, `EquipmentDetailDto` | 動作 + 實體 + Dto 結尾 |
| Repository 介面 | `IWorkOrderRepository` | I 開頭，實體名詞 + Repository |
| Repository 實作 | `WorkOrderRepository` | 對應介面名 |
| Service 介面 | `IWorkOrderService` | I 開頭 |
| Service 實作 | `WorkOrderService` | 對應介面名 |
| Controller | `WorkOrderController` | API 控制器，對應 Service 命名 |
| Razor 頁面 | `WorkOrderPage.razor`, `EditWorkOrderDialog.razor` | 功能 + Page 或 Dialog 結尾 |

---

## 🗂️ Blazor 頁面命名建議

| 類型 | 命名規則 |
|------|----------|
| 列表頁 | `EquipmentPage.razor` |
| 新增 / 編輯 Dialog | `EditEquipmentDialog.razor` |
| 查詢用元件 | `EquipmentFilterPanel.razor` |
| 表單元件 | `EquipmentForm.razor` |

---

## 📌 其他建議

- **資料庫欄位命名：** 建議用 `Snake_Case` 或 `PascalCase`，但程式碼一律使用 PascalCase 對應
- **Enum 命名：** 使用單數名詞（如 `EquipmentStatus`），欄位以 `Status` 結尾
- **介面命名：** 所有介面皆以 `I` 開頭，並與實作類別對應
- **命名語意：** 能清楚反映實體 / 行為功能（例如 `SubmitWorkOrder()` 而不是 `Process()`）

---

## 📘 範例模組命名總覽（以 Equipment 為例）

```
ZeroMES.Equipment/
├── Entities/
│   └── Equipment.cs
├── Dtos/
│   └── EquipmentDetailDto.cs
├── Repositories/
│   ├── IEquipmentRepository.cs
│   └── EquipmentRepository.cs
├── Services/
│   ├── IEquipmentService.cs
│   └── EquipmentService.cs
├── API/
│   └── EquipmentController.cs
├── Client/
│   ├── EquipmentPage.razor
│   ├── EditEquipmentDialog.razor
│   └── EquipmentForm.razor
```
