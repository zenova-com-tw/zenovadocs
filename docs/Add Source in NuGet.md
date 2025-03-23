---
title: 在 NuGet 中添加來源
nav_order: 1
parent: Zenova Centre
---

在 **NuGet** 中新增 **Source（來源）** 的方法有幾種方式，包括使用 **Visual Studio GUI**、**dotnet CLI** 或直接編輯 `nuget.config` 文件。以下是詳細步驟：

---

## 1️⃣ **使用 Visual Studio GUI 新增 NuGet Source**
如果你使用 **Visual Studio**，可以透過 GUI 介面新增 NuGet 套件來源：

### 📌 **步驟**
1. 打開 **Visual Studio**。
2. 在選單中點擊 **工具（Tools）** → **選項（Options）**。
3. 展開 **NuGet 套件管理員（NuGet Package Manager）** → 點擊 **套件來源（Package Sources）**。
4. 在右上角點擊 **+（新增）** 按鈕。
5. 在 **名稱（Name）** 欄位輸入：
   ```
   github-zenova
   ```
6. 在 **來源（Source）** 欄位輸入：
   ```
   https://nuget.pkg.github.com/zenova-com-tw/index.json
   ```
7. 點擊 **更新（Update）**，然後點擊 **確定（OK）**。

💡 **這樣就成功將 GitHub Packages 的 NuGet Source 加入 Visual Studio 內部管理的來源！**

---

## 2️⃣ **使用 dotnet CLI 新增 NuGet Source**
如果你使用的是 **.NET CLI**，可以透過以下指令新增 NuGet Source：

```sh
dotnet nuget add source "https://nuget.pkg.github.com/zenova-com-tw/index.json" --name "github-zenova" --username "YOUR_GITHUB_USERNAME" --password "YOUR_GITHUB_PERSONAL_ACCESS_TOKEN" --store-password-in-clear-text
```

🔹 **參數說明**：
- `--name`：指定 Source 名稱（例如 `github-zenova`）。
- `--username`：你的 GitHub 使用者名稱（但 GitHub Packages 不需要真實的帳號名稱，通常填 **"USERNAME"** 即可）。
- `--password`：你的 **GitHub Personal Access Token（PAT）**，需要擁有 `read:packages` 權限。
- `--store-password-in-clear-text`：允許儲存密碼（不推薦在公用機器上使用）。

---

## 3️⃣ **手動編輯 `nuget.config`**
如果你需要手動修改 **`nuget.config`** 來新增 NuGet 來源，可以按照以下步驟：

### 📌 **步驟**
1. 打開專案目錄（或全域 NuGet 設定的 `%AppData%\NuGet\NuGet.config`）。
2. 找到或建立 **`nuget.config`** 檔案。
3. 在 `<configuration>` 區塊內加入以下內容：

```xml
<configuration>
  <packageSources>
    <add key="github-zenova" value="https://nuget.pkg.github.com/zenova-com-tw/index.json" />
  </packageSources>
  <packageSourceCredentials>
    <github-zenova>
      <add key="Username" value="USERNAME" />
      <add key="ClearTextPassword" value="YOUR_GITHUB_PERSONAL_ACCESS_TOKEN" />
    </github-zenova>
  </packageSourceCredentials>
</configuration>
```

🔹 **注意**：
- `USERNAME` → 這裡應該是 `"USERNAME"`（GitHub Packages 預設接受此值）。
- `YOUR_GITHUB_PERSONAL_ACCESS_TOKEN` → 你需要到 GitHub 產生 **Personal Access Token (PAT)**，並至少賦予 `read:packages` 權限。

---

## 4️⃣ **驗證是否新增成功**
新增 NuGet Source 後，你可以透過以下方式驗證是否成功：

🔹 **使用 CLI 檢查**
```sh
dotnet nuget list source
```
如果成功，應該會顯示：
```
  github-zenova [Enabled]
      https://nuget.pkg.github.com/zenova-com-tw/index.json
```

🔹 **使用 Visual Studio 檢查**
- **打開 Visual Studio** → **工具** → **NuGet 套件管理員** → **套件來源**
- 檢查 **github-zenova** 是否在列表內。

---

## 5️⃣ **在 `.csproj` 中使用 GitHub Packages NuGet 套件**
如果你已經設定好 NuGet 來源，接下來可以在 **`.csproj`** 檔案中加入對應的 NuGet 套件：

```xml
<ItemGroup>
  <PackageReference Include="Your.Package.Name" Version="x.y.z" />
</ItemGroup>
```

如果專案無法成功拉取 GitHub Packages，請確認你已經在 **`nuget.config`** 設定了 `packageSourceCredentials`。

---

## 🔥 **總結**
| 方法 | 操作方式 |
|------|--------|
| **Visual Studio GUI** | 透過 NuGet 套件管理員新增 Source |
| **dotnet CLI** | `dotnet nuget add source ...` |
| **編輯 `nuget.config`** | 手動新增 `<packageSources>` |

這樣就可以成功新增 **GitHub Packages NuGet Source** 並下載私有 NuGet 套件！🚀

