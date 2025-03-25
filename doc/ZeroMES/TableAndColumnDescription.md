---
title: 4. ZeroMES 表格說明
nav_order: 4
parent: ZeroMES 架構文件
grand_parent: 文件中心
---

---

## `assembly_line`（產線主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| description | character varying | 描述說明 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `assembly_line_station`（產線配置資料）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| assembly_line_uid | character varying | 線別的唯一識別碼 |
| sequence | character varying | 順序編號 |
| station | character varying | 線別執行站點 |
| station_type | character varying | 站點類型（如自動/手動） |
| equipment_uid | character varying | 設備代碼 |
| required_user_qty | integer | 要求數量 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `attribute_instance`（屬性資料定義）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| object_id | integer | 對應實體的識別碼 |
| function_name | character varying | 功能名稱 |
| attribute_template_id | integer | 屬性範本識別碼 |
| name | character varying | 名稱 |
| value | character varying | 欄位值 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `attribute_template`（屬性資料範本）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| function_name | character varying | 功能名稱 |
| name | character varying | 名稱 |
| data_type | character varying | 參數或數據的類型，例如數值、文字、日期等，描述資料格式。 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| description | character varying | 描述說明 |
| is_required | boolean | 是否為必填欄位 |
| status | character varying | 狀態，例如啟用/停用 |
| data_safe | integer | 數據安全標誌。 |

---

## `equipment`（設備主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| current_state | character varying | 目前狀態，例如機台或工件的當前狀態 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| owner | character varying | 擁有者 |
| department | character varying | 所屬部門 |
| manufacturer | character varying | 製造商名稱 |
| equipment_model | character varying | 設備型號 |
| asset_id | character varying | 對應實體的代碼或識別碼 |
| description | character varying | 描述說明 |
| processing_type | character varying | 處理類型 |
| processing_mode | character varying | 處理模式 |
| job_type | character varying | 工單類型 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| factory | character varying | 所屬工廠代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `equipment_class`（設備分類資料）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| equipment_class_uid | character varying | 機台類型識別碼 |
| name | character varying | 名稱 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| description | character varying | 描述說明 |
| data_safe | integer | 數據安全標誌。 |

---

## `equipment_group`（設備群組主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| status | character varying | 狀態，例如啟用/停用 |
| description | character varying | 描述說明 |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `equipment_group_eqp`（設備群組與設備對應表）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| equipment_group_uid | character varying | 機台群組識別碼 |
| equipment_uid | character varying | 設備代碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `language`（語系設定資料）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| language_code | character varying | 語言碼 |
| name | character varying | 名稱 |
| value | character varying | 欄位值 |
| category | character varying | UI/MSG |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `material`（待補充）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| type | character varying | 類型（依場景可能代表設備、工單、物料等分類） |
| specification | character varying | 規格說明，例如尺寸、型號或標準 |
| unit | character varying | 單位（如pcs/kg） |
| is_purchased | boolean | 是否外購 |
| is_manufactured | boolean | 是否自製 |
| description | character varying | 描述說明 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |
| classification | character varying | 分類 |

---

## `material_event`（紀錄物料的事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 事件的唯一標識符，用於與其他系統進行數據對應。 |
| event_name | character varying | 事件名稱，描述此記錄的事件名稱。 |
| material_stock_uid | character varying | 關聯的物料庫存明細的唯一標識符。 |
| wip_uid | character varying | 關聯在製品的唯一標識符。 |
| process_uid | character varying | 關聯的工藝 (Process) 唯一標識符。 |
| process_name | character varying | 工藝名稱，用於描述當前工藝的名稱。 |
| quantity | numeric | 與事件相關的物料數量，支持精確到小數點三位。 |
| event_time | character varying | 事件時間，表示此事件的發生時間。 |
| equipment_uid | character varying | 關聯的設備 (Equipment) 唯一標識符。 |
| equipment_name | character varying | 設備名稱，用於描述事件相關的設備名稱。 |
| data_safe | integer | 數據安全標誌。 |
| job_uid | character varying | 關聯的工作 (Job) 唯一標識符。 |
| reference_uid | character varying | 參考唯一標識符，用於關聯其他相關事件中的記錄。 |

---

## `material_location`（倉庫儲位主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| warehouse_uid | character varying | 倉庫唯一標識碼 |
| warehouse | character varying | 倉庫 |
| storage_location | character varying | 倉庫儲位 |
| description | character varying | 儲位說明 |
| created_time | character varying | 建立時間 |
| created_user_uid | character varying | 建立使用者唯一標識碼 |
| last_updated_user_uid | character varying | 最後異動使用者唯一標識碼 |
| last_updated_time | character varying | 最後異動時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `material_process_flow`（物料對應製程流程）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| material_id | integer | 物料識別碼 |
| process_flow_id | integer | 流程識別碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `material_production_spec`（物料對應生產規格）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| material_uid | character varying | 物料代碼 |
| production_spec_uid | character varying | 生產規格代碼 |
| apply_start_date | character varying | 啟用日期 |
| apply_end_date | character varying | 停用日期 |
| created_user_uid | character varying | 啟用日期 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |

---

## `material_stock`（庫存記錄檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 唯一標識符。 |
| warehouse_uid | character varying | 倉庫唯一標識符，用於標識庫存所屬的倉庫。 |
| warehouse | character varying | 倉庫名稱。 |
| storage_location_uid | character varying | 儲位唯一標識符，用於標識具體存放的儲位。 |
| storage_location | character varying | 儲位名稱。 |
| material_uid | character varying | 物料唯一標識符，用於標識物料的 ID。 |
| material_name | character varying | 物料名稱，表示物料的描述性名稱。 |
| material_type | character varying | 物料類型。 |
| internal_batch_uid | character varying | 內部批次唯一標識符，用於追蹤內部批次的數據。 |
| customer_batch_uid | character varying | 客戶批次唯一標識符，用於記錄客戶相關的批次信息。 |
| erp_batch_uid | character varying | ERP 系統中的批次唯一標識符，用於對應企業資源規劃系統中的批次。 |
| receiving_note_no | character varying | 收貨單號，用於記錄該庫存的收貨單據編號。 |
| receiving_status | character varying | 收貨狀態，例如：Pending（待收貨）、Completed（已完成）。 |
| receiving_date | character varying | 收貨日期，表示物料到達或接收的日期。 |
| expiry_date | character varying | 到期日期，用於記錄物料的有效期（如果適用）。 |
| quantity | numeric | 庫存數量，表示當前的庫存總量。 |
| unit_code | character varying | 單位代碼，例如 kg, pcs，表示數量的計量單位。 |
| reserved_quantity | numeric | 已預留的庫存數量，可能為特定訂單或計劃保留。 |
| available_quantity | numeric | 可用的庫存數量，通常等於 quantity - reserved_quantity。 |
| status | character varying | 庫存狀態，例如：Available（可用）、Damaged（損壞）。 |
| created_time | character varying | 記錄創建的時間。 |
| created_user_uid | character varying | 創建記錄的使用者唯一標識符。 |
| last_updated_user_uid | character varying | 最後更新此記錄的使用者唯一標識符。 |
| last_updated_time | character varying | 最後更新的時間。 |
| data_safe | integer | 數據安全標誌。 |

---

## `material_warehouse`（倉庫主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| warehouse | character varying | 倉庫 |
| description | character varying | 說明 |
| created_time | character varying | 建立時間 |
| created_user_uid | character varying | 建立使用者唯一標識碼 |
| last_updated_user_uid | character varying | 最後異動使用者唯一標識碼 |
| last_updated_time | character varying | 最後異動時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `parameter`（參數主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| class | character varying | 分類 |
| name | character varying | 名稱 |
| data_type | character varying | 參數或數據的類型，例如數值、文字、日期等，描述資料格式。 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| description | character varying | 描述說明 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| data_safe | integer | 數據安全標誌。 |

---

## `privilege`（權限設定資料）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| privilege_uid | character varying | 權限識別碼 |
| name | character varying | 名稱 |
| path | character varying | 路徑 |
| description | character varying | 描述說明 |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| privilege_class | character varying | 權限類型 |
| icon | character varying | 圖示名稱 |
| data_safe | integer | 數據安全標誌。 |

---

## `process`（製程階段主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| type | character varying | 類型（依場景可能代表設備、工單、物料等分類） |
| description | character varying | 描述說明 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| process_type | character varying | 製程類型，如自動、手動、半自動等 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `process_flow`（製程流程主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| name | character varying | 名稱 |
| type | character varying | 類型（依場景可能代表設備、工單、物料等分類） |
| description | character varying | 描述說明 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `process_flow_process`（製程流程與製程對應）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| process_flow_uid | character varying | 對應實體的唯一識別碼 |
| process_flow_version_uid | character varying | 對應實體的唯一識別碼 |
| process_uid | character varying | 製程代碼 |
| sequence | character varying | 順序編號 |
| process_type | character varying | 製程類型，如自動、手動、半自動等 |
| data_safe | integer | 數據安全標誌。 |
| uid | character varying | 使用者定義的唯一代碼 |

---

## `process_flow_version`（製程流程版本）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| process_flow_uid | character varying | 對應實體的唯一識別碼 |
| version | integer | 版本 |
| is_activated | boolean | 是否啟用 |
| is_major | boolean | 主要版本 |
| status | character varying | 狀態，例如啟用/停用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `production_spec`（產品規格主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| material_uid | character varying | 物料代碼 |
| uid | character varying | 使用者定義的唯一代碼 |
| apply_start_date | character varying | 啟用日期 |
| apply_end_date | character varying | 停用日期 |
| type | character varying | 啟用日期 |
| is_major | boolean | 主要版本 |
| revision | integer | 版次 |
| ref_spec_uid | character varying | 參考規格識別碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| status | character varying | 狀態，例如啟用/停用 |
| data_safe | integer | 數據安全標誌。 |
| is_activated | boolean | 是否啟用 |

---

## `production_spec_prc`（製程規格主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| production_spec_uid | character varying | 生產規格代碼 |
| process_uid | character varying | 製程代碼 |
| from_seqence | character varying | 來源順序 |
| to_sequene | character varying | 目的順序 |
| data_safe | integer | 數據安全標誌。 |

---

## `production_spec_prc_dc`（製程規格資料收集設定）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 該筆參數記錄的唯一識別字串，可用於追蹤或參照。 |
| production_spec_uid | character varying | 參照 production_spec 表中規格的唯一識別碼，表示此記錄所屬的生產規格。 |
| name | character varying | 參數名稱，用於描述此參數記錄對應的參數。 |
| object_low_spec | numeric | 物件的最低規格值，用來定義品質或參數的下限。 |
| object_target | numeric | 物件的目標規格值，即理想的參數標準。 |
| object_upper_spec | numeric | 物件的最高規格值，用來定義品質或參數的上限。 |
| object_sample_size | numeric | 樣本尺寸或取樣量，代表在生產過程中用於檢測或統計的樣本數量。 |
| data_type | character varying | 參數或數據的類型，例如數值、文字、日期等，描述資料格式。 |
| uom | character varying | 計量單位（Unit of Measure），例如 mm、kg、pcs 等。 |
| description | character varying | 記錄的說明文字，提供對該參數或規格的詳細描述。 |
| is_required | boolean | 指示該參數是否為必填項，true 表示必填，false 表示非必填。 |
| status | character varying | 記錄狀態，如啟用、停用或草稿，用於表示該記錄目前的狀態。 |
| created_user_uid | character varying | 建立此記錄的使用者識別碼。 |
| created_time | character varying | 記錄建立的時間，格式通常為 YYYY-MM-DD HH:MI:SS。 |
| last_updated_user_uid | character varying | 最後更新此記錄的使用者識別碼。 |
| last_updated_time | character varying | 記錄最後更新的時間。 |
| data_safe | integer | 數據安全標誌。 |

---

## `production_spec_prc_eqp`（製程與設備對應規格）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| production_spec_uid | character varying | 生產規格代碼 |
| production_spec_prc_uid | character varying | 製程流程識別碼 |
| equipment_group_uid | character varying | 機台群組識別碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `production_spec_prc_mat`（製程與物料對應規格）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| production_spec_uid | character varying | 生產規格代碼 |
| material_uid | character varying | 物料代碼 |
| required_quantity | numeric | 數量 |
| alternative_material_uid | character varying | 替代物料識別碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_update_user_uid | character varying | 最後異動使用者識別碼 |
| last_update_time | character varying | 日期 |
| data_safe | integer | 數據安全標誌。 |
| production_spec_prc_uid | character varying | 製程流程識別碼 |

---

## `production_spec_prc_tool`（製程與治具對應規格）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| production_spec_uid | character varying | 生產規格代碼 |
| production_spec_prc_uid | character varying | 製程流程識別碼 |
| tool_uid | character varying | 工具代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `reason_category`（異常分類主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| description | character varying | 描述說明 |
| status | character varying | 狀態，例如啟用/停用 |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `reason_category_reasoncode`（異常分類與代碼對應）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| reason_category_uid | character varying | 原因碼分類識別碼 |
| uid | character varying | 使用者定義的唯一代碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `reason_setting`（異常代碼與處理方式設定）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| object_type | character varying | 對應物件類型 |
| object_uid | character varying | 物件識別碼，例如追蹤的工件或資源代碼 |
| controlevent | character varying | 控制事件代碼 |
| category_uid | character varying | 分類識別碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `receive`（收料單主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 收料單號 |
| po_uid | character varying | 訂單編號 |
| supplier_uid | character varying | 廠商編號 |
| receive_date | character varying | 收貨日期，表示物料到達或接收的日期。 |
| status | character varying | 收貨狀態，例如：Pending（待收貨）、Completed（已完成） |
| is_activated | boolean | 是否啟用 |
| created_user_uid | character varying | 建立人員帳號 |
| created_time | character varying | 建立時間 |
| last_updated_user_uid | character varying | 更新人員帳號 |
| last_updated_time | character varying | 更新時間 |
| data_safe | integer | 數據安全標誌。 |
| description | character varying | 描述說明 |

---

## `receive_material`（收料明細）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| receive_uid | character varying | 收料單系統編號 |
| sequence | integer | 項次序號 |
| material_uid | character varying | 物料料號 |
| quantity | numeric | 應收數量 |
| actual_quantity | numeric | 實收數量 |
| erp_batch_uid | character varying | ERP 系統中的批次唯一標識符，用於對應企業資源規劃系統中的批次。 |
| receive_type | character varying | 收料類型 |
| created_user_uid | character varying | 建立人員帳號 |
| created_time | character varying | 建立時間 |
| last_updated_user_uid | character varying | 更新人員帳號 |
| last_updated_time | character varying | 更新時間 |
| data_safe | integer | 數據安全標誌。 |
| customer_batch_uid | character varying | 客戶批次唯一標識符，用於記錄客戶相關的批次信息。 |
| expiry_date | character varying | 到期日期，用於記錄物料的有效期 |
| stock_uid | character varying | 倉庫唯一標識符，用於標識庫存所屬的倉庫。 |
| storage_location_uid | character varying | 儲位唯一標識符，用於標識具體存放的儲位。 |

---

## `role`（角色主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| role_uid | character varying | 角色識別碼 |
| name | character varying | 名稱 |
| description | character varying | 描述說明 |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `role_privilege`（權限設定資料）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| privilege_id | integer | 權限識別碼 |
| role_id | integer | 角色識別碼 |
| permission_type | character varying | 權限型態 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character varying | 資料建立時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `setting`（系統參數設定）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| class | character varying | 分類 |
| name | character varying | 名稱 |
| value | character varying | 欄位值 |
| description | character varying | 描述說明 |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| read_only | boolean | 是否唯讀 |
| data_safe | integer | 數據安全標誌。 |

---

## `tool`（治具主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 模治具編號 |
| name | character varying | 模治具名稱 |
| type | character varying | 模具治類型 |
| specification | character varying | 規格描述 |
| default_storage_location | character varying | 預設儲位 |
| current_state | character varying | 目前模治具狀態 |
| is_activated | boolean | 曾經啟用IY/N) |
| status | character varying | 模治具目前是否啟用(Y/N) |
| owner | character varying | 模治具負責人 |
| department | character varying | 所屬部門 |
| description | character varying | 說明 |
| manufacturer | character varying | 製造商 |
| life_cycle_limit | integer | 模治具可用次數 |
| usage_count | integer | 目前已使用次數 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |
| current_storage_location | character varying | 當前儲位 |
| last_event_uid | character varying | 最近一次事件的代碼 |
| last_event_name | character varying | 最近事件名稱，例如「開始」、「暫停」、「完成」等 |
| custom_field_01 | character varying | 自定義欄位 1 |
| custom_field_02 | character varying | 自定義欄位 2 |
| custom_field_03 | character varying | 自定義欄位 3 |
| custom_field_04 | character varying | 自定義欄位 4 |
| custom_field_05 | character varying | 自定義欄位 5 |
| custom_field_06 | character varying | 自定義欄位 6 |
| custom_field_07 | character varying | 自定義欄位 7 |
| custom_field_08 | character varying | 自定義欄位 8 |
| custom_field_09 | character varying | 自定義欄位 9 |
| custom_field_10 | character varying | 自定義欄位 10 |
| previous_state | character varying | 前狀態 |
| ToolCategory | character varying | 大分類(模具:M、治具:F、刀具:T) |

---

## `tool_equipment`（設備主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| tool_uid | character varying | 工具代碼 |
| equipment_uid | character varying | 設備代碼 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `tool_event`（設備事件主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| tool_uid | character varying | 模治具唯一編號 |
| event_name | character varying | 事件名稱 |
| event_time | character varying | 事件發生時間 |
| equipment_uid | character varying | 設備代碼 |
| wip_uid | character varying | 在製品（WIP）代碼 |
| data_safe | integer | 數據安全標誌。 |
| privilege_uid | character varying | 權限識別碼 |
| uid | character varying | 使用者定義的唯一代碼 |
| event_worker_uid | character varying | 事件人員識別碼 |

---

## `tool_event_pause`（設備暫停事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| event_uid | character varying | 事件代碼 |
| tool_uid | character varying | 工具代碼 |
| reason_category_uid | character varying | 原因碼分類識別碼 |
| reason_category_reasoncode_uid | character varying | 原因分類與代碼，例如異常分類代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `tool_event_repair`（設備維修事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| event_uid | character varying | 事件代碼 |
| tool_uid | character varying | 工具代碼 |
| issue_reason_category_uid | character varying | 原因碼分類識別碼 |
| issue_reason_category_reasoncode_uid | character varying | 分類原因碼識別碼 |
| state | character varying | 狀態 |
| repair_reason_category_uid | character varying | 維修原因碼分類碼識別碼 |
| repair_reason_category_reasoncode_uid | character varying | 維修原因碼識別碼 |
| description | character varying | 描述說明 |
| data_safe | integer | 數據安全標誌。 |

---

## `tool_snap`（治具即時狀態快照）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 模治具編號 |
| name | character varying | 模治具名稱 |
| type | character varying | 模具治類型 |
| specification | character varying | 規格描述 |
| default_storage_location | character varying | 預設儲位 |
| current_state | character varying | 目前模治具狀態 |
| is_activated | boolean | 曾經啟用IY/N) |
| status | character varying | 模治具目前是否啟用(Y/N) |
| owner | character varying | 模治具負責人 |
| department | character varying | 所屬部門 |
| description | character varying | 說明 |
| manufacturer | character varying | 製造商 |
| life_cycle_limit | integer | 模治具可用次數 |
| usage_count | integer | 目前已使用次數 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |
| current_storage_location | character varying | 當前儲位 |
| last_event_uid | character varying | 最近一次事件的代碼 |
| last_event_name | character varying | 最近事件名稱，例如「開始」、「暫停」、「完成」等 |
| custom_field_01 | character varying | 自定義欄位 1 |
| custom_field_02 | character varying | 自定義欄位 2 |
| custom_field_03 | character varying | 自定義欄位 3 |
| custom_field_04 | character varying | 自定義欄位 4 |
| custom_field_05 | character varying | 自定義欄位 5 |
| custom_field_06 | character varying | 自定義欄位 6 |
| custom_field_07 | character varying | 自定義欄位 7 |
| custom_field_08 | character varying | 自定義欄位 8 |
| custom_field_09 | character varying | 自定義欄位 9 |
| custom_field_10 | character varying | 自定義欄位 10 |
| previous_state | character varying | 前狀態 |

---

## `user`（使用者主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| user_uid | character varying | 使用者識別碼 |
| name | character varying | 名稱 |
| password | character varying | 密碼欄位 |
| description | character varying | 描述說明 |
| email | character varying | 電子郵件地址 |
| status | character varying | 狀態，例如啟用/停用 |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_password_updated_time | character varying | 日期 |
| data_safe | integer | 數據安全標誌。 |

---

## `user_role`（角色主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| user_id | integer | 使用者唯一碼 |
| role_id | integer | 角色識別碼 |
| created_time | character varying | 資料建立時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `wip_event`（A table that records all event related production, such as StartingOperation, EndOperation, Split,_x000D_
Merge etc ...）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| wip_uid | character varying | 在製(work_in_process)唯一編號 |
| event_name | character varying | 事件名稱 |
| quantity | numeric | 數量 |
| event_time | character varying | 事件發生時間 |
| equipment_uid | character varying | 設備代碼 |
| process_uid | character varying | 製程代碼 |
| production_spec_revision | integer | 生產規格版本 |
| previous_operation_uid | character varying | 前站點識別碼 |
| workorder_uid | character varying | 工單代碼 |
| data_safe | integer | 數據安全標誌。 |
| job_uid | character varying | 任務代碼 |
| privilege_uid | character varying | 權限識別碼 |
| uid | character varying | 使用者定義的唯一代碼 |
| event_worker_uid | character varying | 事件人員識別碼 |

---

## `wip_event_defect`（WIP 缺陷事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| event_uid | character varying | 事件唯一編號 |
| wip_uid | character varying | 在製唯一編號 |
| reason_category_reasoncode_uid | character varying | 原因碼編號 |
| quantity | numeric | 數量 |
| process_uid | character varying | 處理編號 |
| reference_process_uid | character varying | 參考處理編號 |
| uid | character varying | 系統唯一編號 |
| reason_category_uid | character varying | 原因碼分類識別碼 |
| scrapquantity | numeric | 數量 |
| ori_reason_category_reasoncode_uid | character varying | 原始不良原因碼分類碼識別碼 |
| ori_reason_category_uid | character varying | 原始不良原因碼識別碼 |

---

## `wip_event_merge`（WIP 合併事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| main_wip_uid | character varying | 主WIP識別碼 |
| sub_wip_uid | character varying | 子WIP識別碼 |
| event_uid | character varying | 事件代碼 |
| quantity | numeric | 數量 |
| process_uid | character varying | 製程代碼 |
| reason_category_uid | character varying | 原因碼分類識別碼 |
| reason_category_reasoncode_uid | character varying | 原因分類與代碼，例如異常分類代碼 |
| quantity2 | numeric | 輔助數量（例如重量、批量） |
| data_safe | integer | 數據安全標誌。 |

---

## `wip_event_scrap`（WIP 報廢事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| event_uid | character varying | 事件唯一編號 |
| wip_uid | character varying | 在製唯一編號 |
| reason_category_reasoncode_uid | character varying | 原因碼編號 |
| quantity | numeric | 數量 |
| process_uid | character varying | 處理編號 |
| reference_process_uid | character varying | 參考處理編號 |
| uid | character varying | 系統唯一編號 |
| reason_category_uid | character varying | 原因碼分類識別碼 |

---

## `wip_event_split`（WIP 拆分事件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| ori_wip_uid | character varying | 原WIP識別碼 |
| sub_wip_uid | character varying | 子WIP識別碼 |
| quantity | numeric | 數量 |
| event_uid | character varying | 事件代碼 |
| quantity2 | numeric | 輔助數量（例如重量、批量） |
| process_uid | character varying | 製程代碼 |
| reason_category_uid | character varying | 原因碼分類識別碼 |
| reason_category_reasoncode_uid | character varying | 原因分類與代碼，例如異常分類代碼 |
| data_safe | integer | 數據安全標誌。 |

---

## `wip_job`（WIP 工作主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | Unique identifier for the job |
| category | character varying | Category of the production control job |
| created_time | character varying | Time when the job was created (string format) |
| created_user_uid | character varying | User UID who created the job |
| finish_time | character varying | Time when the job was finished (string format) |
| finish_user_uid | character varying | User UID who finished the job |
| equipment_uid | character varying | UID of the equipment used in the job |
| equipment_name | character varying | Name of the equipment used in the job |
| data_safe | integer | 數據安全標誌。 |
| last_updated_time | character varying | 最後資料更新時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |

---

## `wip_job_object`（WIP 工作物件）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 唯一標識碼，UUID 格式 |
| category | character varying | 分類，用於標識此工作的類別 |
| job_uid | character varying | 對應的工作唯一標識碼 |
| object_category | character varying | 生產對象類型，例如批號、工單等 |
| object_uid | character varying | 生產對象的唯一標識碼 |
| material_name | character varying | 材料名稱 |
| material_type | character varying | 材料類型 |
| start_job_event_uid | character varying | 起始工作事件的唯一標識碼 |
| start_job_event_step | character varying | 起始工作事件的步驟名稱 |
| start_job_event_name | character varying | 起始工作事件的名稱 |
| start_job_event_time | character varying | 起始工作事件的時間 |
| start_job_user_uid | character varying | 起始工作事件操作用戶的唯一標識碼 |
| start_job_user_name | character varying | 起始工作事件操作用戶的名稱 |
| start_job_event_remark01 | character varying | 起始工作事件備註1 |
| start_job_event_remark02 | character varying | 起始工作事件備註2 |
| start_job_event_remark03 | character varying | 起始工作事件備註3 |
| start_job_event_remark04 | character varying | 起始工作事件備註4 |
| start_job_event_remark05 | character varying | 起始工作事件備註5 |
| job_start_time | character varying | 工作的開始時間 |
| job_start_uom | character varying | 生產對象的起始單位，例如公斤，顆數 |
| job_start_quantity | numeric | 工作的開始數量 |
| from_process_uid | character varying | 來源工序編號 |
| from_process_sequence | character varying | 來源工序在生產流程中的順序 |
| job_status | character varying | 工作的當前狀態，例如進行中、已完成 |
| job_split_quantity | numeric | 工作分解的數量 |
| job_adjust_quantity | numeric | 工作調整的數量 |
| job_scrap_quantity | numeric | 工作報廢的數量 |
| parent_object_uid | character varying | 父對象的唯一標識碼 |
| rework | character varying | 是否為返工(Y/N) |
| work_order_uid | character varying | 工單的唯一標識碼 |
| manufacturing_type | character varying | 生產類型，例如量產品或工程實驗品 |
| job_type | character varying | 工作的類型，例如單批 / 批次 / 連續產出 |
| control_mode | character varying | 控制模式，例如自動生產、手動生產 |
| process_type | character varying | 工藝類型，例如加工製程、檢測製程 |
| equipment_uid | character varying | 設備的唯一標識碼 |
| equipment_name | character varying | 設備名稱 |
| data_safe | integer | 數據安全標誌。 |
| production_spec_revision | integer | 製程設定版本 |
| production_spec_uid | character varying | 製程設定編號 |

---

## `wip_job_object_done`（WIP 工作物件完成記錄）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 唯一標識碼，UUID 格式 |
| category | character varying | 分類，用於標識此工作的類別 |
| job_uid | character varying | 對應的工作唯一標識碼 |
| object_category | character varying | 生產對象類型，例如批號、工單等 |
| object_uid | character varying | 生產對象的唯一標識碼 |
| material_name | character varying | 材料名稱 |
| material_type | character varying | 材料類型 |
| start_job_event_uid | character varying | 起始工作事件的唯一標識碼 |
| start_job_event_step | character varying | 起始工作事件的步驟名稱 |
| start_job_event_name | character varying | 起始工作事件的名稱 |
| start_job_event_time | character varying | 起始工作事件的時間 |
| start_job_user_uid | character varying | 起始工作事件操作用戶的唯一標識碼 |
| start_job_user_name | character varying | 起始工作事件操作用戶的名稱 |
| start_job_event_remark01 | character varying | 起始工作事件備註1 |
| start_job_event_remark02 | character varying | 起始工作事件備註2 |
| start_job_event_remark03 | character varying | 起始工作事件備註3 |
| start_job_event_remark04 | character varying | 起始工作事件備註4 |
| start_job_event_remark05 | character varying | 起始工作事件備註5 |
| job_start_time | character varying | 工作的開始時間 |
| job_start_uom | character varying | 生產對象的起始單位，例如公斤，顆數 |
| job_start_quantity | numeric | 工作的開始數量 |
| from_process_uid | character varying | 來源工序編號 |
| from_process_sequence | character varying | 來源工序在生產流程中的順序 |
| end_job_event_uid | character varying | 結束工作事件的唯一標識碼 |
| end_job_event_step | character varying | 結束工作事件的步驟名稱 |
| end_job_event_name | character varying | 結束工作事件的名稱 |
| end_job_event_time | character varying | 結束工作事件的時間 |
| end_job_user_uid | character varying | 結束工作事件操作用戶的唯一標識碼 |
| end_job_user_name | character varying | 結束工作事件操作用戶的名稱 |
| end_job_event_remark01 | character varying | 結束工作事件備註1 |
| end_job_event_remark02 | character varying | 結束工作事件備註2 |
| end_job_event_remark03 | character varying | 結束工作事件備註3 |
| end_job_event_remark04 | character varying | 結束工作事件備註4 |
| end_job_event_remark05 | character varying | 結束工作事件備註5 |
| job_end_time | character varying | 工作的結束時間 |
| job_end_uom | character varying | 生產對象的結束單位，例如公斤，顆數 |
| job_end_quantity | numeric | 工作的結束數量 |
| to_process_uid | character varying | 目的工序 |
| to_process_sequence | character varying | 目的工序在生產流程中的順序 |
| job_status | character varying | 工作的當前狀態，例如進行中、已完成 |
| job_split_quantity | numeric | 工作分解的數量 |
| job_adjust_quantity | numeric | 工作調整的數量 |
| job_scrap_quantity | numeric | 工作報廢的數量 |
| job_process_time | integer | 工作的處理時間，單位為秒 |
| parent_object_uid | character varying | 父對象的唯一標識碼 |
| rework | character varying | 是否為返工(Y/N) |
| work_order_uid | character varying | 工單的唯一標識碼 |
| manufacturing_type | character varying | 生產類型，例如量產品或工程實驗品 |
| job_type | character varying | 工作的類型，例如單批 / 批次 / 連續產出 |
| control_mode | character varying | 控制模式，例如自動生產、手動生產 |
| process_type | character varying | 工藝類型，例如加工製程、檢測製程 |
| equipment_uid | character varying | 設備的唯一標識碼 |
| equipment_name | character varying | 設備名稱 |
| data_safe | integer | 數據安全標誌。 |
| production_spec_revision | integer | 製程設定版本 |
| production_spec_uid | character varying | 製程設定編號 |

---

## `work_in_process`（WIP 主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 在製唯一編號 |
| material_uid | character varying | 料號 |
| material_name | character varying | 料號名稱 |
| material_type | character varying | 料號類型 |
| production_spec_uid | character varying | 製程設定編號 |
| process_uid | character varying | 製程編號 |
| production_spec_revision | integer | 製程設定版本 |
| workorder_uid | character varying | 工單編號 |
| created_time | character varying | 建立時間 |
| created_user_uid | character varying | 建立人員編號 |
| created_user_name | character varying | 建立人員姓名 |
| production_order_uid | character varying | 生產訂單編號 |
| quantity | numeric | 主數量 |
| quantity2 | numeric | 次數量 |
| uom | character varying | 主計量單位 |
| uom2 | character varying | 次計量單位 |
| process_sequence | character varying | 製程順序 |
| process_step_uid | character varying | 製程步驟編號 |
| process_step_name | character varying | 製程步驟名稱 |
| process_step_sequence | integer | 製程步驟順序 |
| step_control_flag | character varying | 階段控制標誌 |
| status | character varying | 狀態
		等待生產 → Pending
		生產中 → Producing
		生產完成 → Completed
		待檢驗 → Inspecting
		待點交 → Handover
		被扣留 → OnHold
		強制結束 → Forced
		取消生產 → Canceled
		暫停生產 → Paused
	 |
| batch_type | character varying | 批次類型(WO/LOT) |
| priority | integer | 優先級 |
| job_uid | character varying | 生產任務編號 |
| job_start_time | character varying | 任務開始時間 |
| job_end_time | character varying | 任務結束時間 |
| last_event_uid | character varying | 最後事件編號 |
| last_event_name | character varying | 最後事件名稱 |
| last_updated_time | character varying | 最後修改時間 |
| last_updated_user_uid | character varying | 最後修改人員編號 |
| last_updated_user_name | character varying | 最後修改人員姓名 |
| defect_count | numeric | 缺陷數量 |
| yield | numeric | 良率 |
| notes | character varying | 備註 |
| parent_wip_uid | character varying | 父在製品唯一編號 |
| qc_status | character varying | 品質檢驗狀態 |
| on_hold | boolean | 是否扣留 |
| hold_reason_code | character varying | 扣留原因代碼 |
| hold_reason_description | character varying | 扣留原因描述 |
| hold_time | character varying | 扣留時間 |
| released_user_uid | character varying | 釋放人員編號 |
| released_user_name | character varying | 釋放人員姓名 |
| released_time | character varying | 釋放時間 |
| hold_resolution_notes | character varying | 扣留解決備註 |
| storage_location | character varying | 儲位 |
| factory | character varying | 工廠 |
| assembly_line | character varying | 生產線 |
| rework | boolean | 是否返工 |
| rework_count | integer | 返工次數 |
| customer_uid | character varying | 客戶編號 |
| customer_name | character varying | 客戶名稱 |
| customer_order_uid | character varying | 客戶訂單編號 |
| due_date | character varying | 交付日期 |
| custom_field_01 | character varying | 自定義欄位 1 |
| custom_field_02 | character varying | 自定義欄位 2 |
| custom_field_03 | character varying | 自定義欄位 3 |
| custom_field_04 | character varying | 自定義欄位 4 |
| custom_field_05 | character varying | 自定義欄位 5 |
| custom_field_06 | character varying | 自定義欄位 6 |
| custom_field_07 | character varying | 自定義欄位 7 |
| custom_field_08 | character varying | 自定義欄位 8 |
| custom_field_09 | character varying | 自定義欄位 9 |
| custom_field_10 | character varying | 自定義欄位 10 |
| data_safe | integer | 數據安全標誌。 |
| previous_status | character varying | 上一個狀態 |

---

## `work_in_process_snap`（WIP 即時狀態快照）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 在製唯一編號 |
| material_uid | character varying | 料號 |
| material_name | character varying | 料號名稱 |
| material_type | character varying | 料號類型 |
| production_spec_uid | character varying | 製程設定編號 |
| process_uid | character varying | 製程編號 |
| production_spec_revision | integer | 製程設定版本 |
| workorder_uid | character varying | 工單編號 |
| created_time | character varying | 建立時間 |
| created_user_uid | character varying | 建立人員編號 |
| created_user_name | character varying | 建立人員姓名 |
| production_order_uid | character varying | 生產訂單編號 |
| quantity | numeric | 主數量 |
| quantity2 | numeric | 次數量 |
| uom | character varying | 主計量單位 |
| uom2 | character varying | 次計量單位 |
| process_sequence | character varying | 製程順序 |
| process_step_uid | character varying | 製程步驟編號 |
| process_step_name | character varying | 製程步驟名稱 |
| process_step_sequence | integer | 製程步驟順序 |
| step_control_flag | character varying | 階段控制標誌 |
| status | character varying | 狀態
		等待生產 → Pending
		生產中 → Producing
		生產完成 → Completed
		待檢驗 → Inspecting
		待點交 → Handover
		被扣留 → OnHold
		強制結束 → Forced
		取消生產 → Canceled
		暫停生產 → Paused
	 |
| batch_type | character varying | 批次類型(WO/LOT) |
| priority | integer | 優先級 |
| job_uid | character varying | 生產任務編號 |
| job_start_time | character varying | 任務開始時間 |
| job_end_time | character varying | 任務結束時間 |
| last_event_uid | character varying | 最後事件編號 |
| last_event_name | character varying | 最後事件名稱 |
| last_updated_time | character varying | 最後修改時間 |
| last_updated_user_uid | character varying | 最後修改人員編號 |
| last_updated_user_name | character varying | 最後修改人員姓名 |
| defect_count | numeric | 缺陷數量 |
| yield | numeric | 良率 |
| notes | character varying | 備註 |
| parent_wip_uid | character varying | 父在製品唯一編號 |
| qc_status | character varying | 品質檢驗狀態 |
| on_hold | boolean | 是否扣留 |
| hold_reason_code | character varying | 扣留原因代碼 |
| hold_reason_description | character varying | 扣留原因描述 |
| hold_time | character varying | 扣留時間 |
| released_user_uid | character varying | 釋放人員編號 |
| released_user_name | character varying | 釋放人員姓名 |
| released_time | character varying | 釋放時間 |
| hold_resolution_notes | character varying | 扣留解決備註 |
| storage_location | character varying | 儲位 |
| factory | character varying | 工廠 |
| assembly_line | character varying | 生產線 |
| rework | boolean | 是否返工 |
| rework_count | integer | 返工次數 |
| customer_uid | character varying | 客戶編號 |
| customer_name | character varying | 客戶名稱 |
| customer_order_uid | character varying | 客戶訂單編號 |
| due_date | character varying | 交付日期 |
| custom_field_01 | character varying | 自定義欄位 1 |
| custom_field_02 | character varying | 自定義欄位 2 |
| custom_field_03 | character varying | 自定義欄位 3 |
| custom_field_04 | character varying | 自定義欄位 4 |
| custom_field_05 | character varying | 自定義欄位 5 |
| custom_field_06 | character varying | 自定義欄位 6 |
| custom_field_07 | character varying | 自定義欄位 7 |
| custom_field_08 | character varying | 自定義欄位 8 |
| custom_field_09 | character varying | 自定義欄位 9 |
| custom_field_10 | character varying | 自定義欄位 10 |
| data_safe | integer | 數據安全標誌。 |
| previous_status | character varying | 上一個狀態 |

---

## `workorder`（工單主檔）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| material_uid | character varying | 物料代碼 |
| material_name | character varying | 物料名稱 |
| material_type | character varying | 物料類型，例如原料、半成品、包裝材料等 |
| production_spec_uid | character varying | 生產規格代碼 |
| batch_type | character varying | 批次類型 |
| production_order_uid | character varying | 生產訂單代碼 |
| quantity | numeric | 數量 |
| quantity2 | numeric | 輔助數量（例如重量、批量） |
| release_quantity | numeric | 數量 |
| uom | character varying | 數量單位（Unit of Measure） |
| uom2 | character varying | 輔助單位 |
| priority | integer | 優先順序 |
| factory | character varying | 所屬工廠代碼 |
| schedule_date | character | 日期 |
| due_date | character varying | 到期日、交期 |
| customer_uid | character varying | 客戶代碼 |
| customer_name | character varying | 客戶名稱 |
| customer_order_uid | character varying | 客戶訂單代碼 |
| notes | character varying | 備註欄位 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| status | character varying | 狀態，例如啟用/停用 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |
| eqp_workorder | character varying | 機台中工單 |
| custom_field_01 | character varying | 自定義欄位 1 |
| custom_field_02 | character varying | 自定義欄位 2 |
| custom_field_03 | character varying | 自定義欄位 3 |
| custom_field_04 | character varying | 自定義欄位 4 |
| custom_field_05 | character varying | 自定義欄位 5 |
| custom_field_06 | character varying | 自定義欄位 6 |
| custom_field_07 | character varying | 自定義欄位 7 |
| custom_field_08 | character varying | 自定義欄位 8 |
| custom_field_09 | character varying | 自定義欄位 9 |
| custom_field_10 | character varying | 自定義欄位 10 |
| production_spec_revision | integer | 生產規格版本 |

---

## `workorder_schedule`（工單排程資訊）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| uid | character varying | 使用者定義的唯一代碼 |
| workorder_uid | character varying | 工單代碼 |
| assign_equipment_uid | character varying | 指派機台識別碼 |
| assign_tool_uid | character varying | 指派配件識別碼 |
| groupid | character varying | 群組代碼 |
| plan_quantity | numeric | 數量 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| status | character varying | 狀態，例如啟用/停用 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |

---

## `worktime_workrecord`（nan）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| equipment_uid | character varying | 設備代碼 |
| worker_uid | character varying | 作業人員識別碼 |
| workorder_uid | character varying | 工單代碼 |
| process_uid | character varying | 製程代碼 |
| wip_uid | character varying | 在製品（WIP）代碼 |
| quantity | numeric | 數量 |
| shiftdate | character varying | 日期 |
| starttime | character varying | 開始時間 |
| endtime | character varying | 結束時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| is_processed | boolean | 是否處理 |
| data_safe | integer | 數據安全標誌。 |

---

## `worktime_workstatus`（人員工時與工作狀態紀錄）

| 欄位名稱 | 資料型態 | 欄位說明 |
|----------|-----------|-----------|
| id | integer | 主鍵，自動生成的唯一標識符。 |
| equipment_uid | character varying | 設備代碼 |
| worker_uid | character varying | 作業人員識別碼 |
| workstatus | character varying | 工作狀態 |
| shiftdate | character varying | 日期 |
| starttime | character varying | 開始時間 |
| endtime | character varying | 結束時間 |
| created_user_uid | character varying | 建立資料的使用者代碼 |
| created_time | character | 資料建立時間 |
| last_updated_user_uid | character varying | 最後更新資料的使用者代碼 |
| last_updated_time | character varying | 最後資料更新時間 |
| data_safe | integer | 數據安全標誌。 |