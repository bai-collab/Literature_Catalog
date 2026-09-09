# 使用 ChatGPT 初始化 Literature Library

此文件供新使用者建立自己的 Literature Library。

## 使用者先做的事

1. 在自己的 Google Drive 建立一個**新的空白資料夾**。
2. 複製該資料夾 URL。
3. 確認 ChatGPT 已連接自己的 Google Drive。
4. 將下方初始化指令貼給 ChatGPT，並把 `<YOUR_GOOGLE_DRIVE_ROOT_URL>` 換成自己的空白資料夾 URL。

## 可直接貼給 ChatGPT 的初始化指令

```text
請初始化我的 Literature Library。

目標 Google Drive 根資料夾：
<YOUR_GOOGLE_DRIVE_ROOT_URL>

公開模板：
https://github.com/bai-collab/Literature_Catalog

請依下列規則執行：

1. 先讀取公開 repository 的 README.md、template/library_structure.yaml、template/catalog_template.yaml，以及 template/00_ADMIN/SKILLS/。
2. 先列出我指定的 Google Drive 根資料夾，確認目前內容與寫入權限。
3. 只在我指定的根資料夾內操作，不得操作其他 Drive 資料夾。
4. 建立缺少的資料夾：
   - 00_ADMIN
   - 00_ADMIN/SKILLS
   - 01_INBOX
   - 10_LIBRARY
   - 80_SYNTHESIS
   - 90_PROJECT_OUTPUT
   - 98_REVIEW_LATER
   - 99_ARCHIVE
5. 依 template/catalog_template.yaml 建立原生 Google Sheet：
   00_ADMIN/00_總書目索引_Literature_Catalog
   並建立四個分頁：總書目、RLC分類表、代碼表、README。
6. 「總書目」只建立欄位標題，不得加入模板以外的任何文獻資料列。
7. 將 template/00_ADMIN/SKILLS/ 的 00_SKILL_REGISTRY.yaml 與 01～10 Skill 建立到我的 00_ADMIN/SKILLS/。
8. 已存在的同名資料夾、Catalog、Registry 或 Skill 不得覆寫。若為部分初始化，只補缺少項目並列出 existing / created / skipped / failed。
9. 不得從任何其他 Google Drive、歷史對話或其他使用者帳號複製 PDF、書目紀錄、分析成果、姓名、Email、Drive ID 或個人資料。
10. 所有建立動作完成後，重新列出 Google Drive 結構並實際讀取 Catalog 與 00_SKILL_REGISTRY.yaml 驗證。
11. 只有驗證成功的項目才能標記完成；失敗項目需明確列出，不得文字宣稱已完成。

最後回報：
- Drive root
- created
- existing/skipped
- failed
- Catalog 是否可讀
- Registry 是否可讀
- 是否可以開始使用 Literature Library
```

## Project Instructions

初始化完成後，開啟 repository 根目錄的 `PROJECT_INSTRUCTIONS.yaml`，只把：

```yaml
storage:
drive_root: "<USER_GOOGLE_DRIVE_ROOT_URL>"
```

中的 placeholder 換成自己的 Google Drive 根資料夾 URL。

其他 Project Instructions 原則上不需修改。

## 注意

- 本 repository 不包含任何正式館藏資料。
- 不要把其他人的 Drive URL 填入自己的 Project Instructions。
- 不要用初始化流程覆寫已經使用中的 Literature Library。
- 若目標資料夾不是空白，ChatGPT 必須先盤點並採「只補缺少項目」策略。
