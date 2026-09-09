# Literature Catalog

可分享的 Literature Library 初始化模板。

本 repository 僅保存**系統架構、Catalog 空白 schema、Skill Registry 與 Skills**，不包含任何原始研究資料或個人資訊。

## 隱私原則

本 repository **不包含**：

- 原始 Google Drive URL 或 folder ID
- 使用者姓名、Email、學校、帳號或其他個人識別資訊
- 已收錄文獻的書目資料列
- 原始 PDF
- Quick Read / Full Analysis / Evidence 等既有分析成果
- `01_INBOX`、`10_LIBRARY`、`80_SYNTHESIS`、`90_PROJECT_OUTPUT`、`98_REVIEW_LATER`、`99_ARCHIVE` 中的既有內容

本 repository **只包含**：

- Literature Library 資料夾架構
- 空白 Catalog schema 與固定分類／代碼設定
- `00_ADMIN/SKILLS` 的 Registry 與 Skill 設定

## 建議初始化方式

1. 使用者先在自己的 Google Drive 建立一個**空白根資料夾**。
2. 將該空白資料夾 URL 提供給 ChatGPT。
3. 要求 ChatGPT 依本 repository 的 `template/library_structure.yaml` 建立資料夾。
4. 依 `template/catalog_template.yaml` 建立原生 Google Sheet：`00_總書目索引_Literature_Catalog`。
5. 將 `template/00_ADMIN/SKILLS/` 內的 Registry 與 Skills 建立到使用者自己的 `00_ADMIN/SKILLS/`。
6. 最後只需把 Literature Library Project Instructions 中的 `storage.drive_root` 改成使用者自己的 Google Drive 根資料夾 URL。

## Google Drive 目標結構

```text
<USER_DRIVE_ROOT>/
├─ 00_ADMIN/
│  ├─ 00_總書目索引_Literature_Catalog
│  └─ SKILLS/
│     ├─ 00_SKILL_REGISTRY.yaml
│     ├─ 01_intake.yaml
│     ├─ 02_quick_read.yaml
│     ├─ 03_full_analysis.yaml
│     ├─ 04_experiment_audit.yaml
│     ├─ 05_domain_agent_harness.yaml
│     ├─ 06_domain_education.yaml
│     ├─ 07_domain_annotation.yaml
│     ├─ 08_synthesis.yaml
│     ├─ 09_library_write.yaml
│     └─ 10_skill_builder.yaml
├─ 01_INBOX/
├─ 10_LIBRARY/
├─ 80_SYNTHESIS/
├─ 90_PROJECT_OUTPUT/
├─ 98_REVIEW_LATER/
└─ 99_ARCHIVE/
```

## 初始化安全規則

- 只對使用者明確指定的空白／目標根資料夾操作。
- 建立前先檢查同名項目。
- 已存在的 Catalog、Registry、Skill 或館藏資料不得覆寫。
- 若為部分初始化狀態，只補缺少項目。
- 初始化完成後重新列出並驗證資料夾、Catalog 與 Registry。
- 未實際成功寫入 Google Drive，不得宣稱初始化完成。

## Repository 結構

- `template/library_structure.yaml`：Drive scaffold manifest。
- `template/catalog_template.yaml`：空白 Google Sheets Catalog 的四分頁 schema/config。
- `template/00_ADMIN/SKILLS/`：可重建到 Google Drive 的 Registry 與 Skills。

> GitHub 不保存空資料夾，因此空的館藏資料夾以 `.gitkeep` 表示；初始化時應建立真正的 Google Drive 資料夾，而不是複製 `.gitkeep`。
