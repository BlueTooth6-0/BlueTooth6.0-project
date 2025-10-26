# BlueTooth6.0 Tests

歡迎來到專案的測試中心。此目錄 (`tests/`) 專為貢獻者（Contributors）設計，用於存放所有確保平台穩定性、模型準確性與程式碼品質的測試腳本。

如果您希望為本專案做出貢獻，在您提交 Pull Request (PR) 之前，請務必在此新增或更新相關的單元測試 (Unit Tests)、整合測試 (Integration Tests) 或功能測試 (Functional Tests)，並確保所有測試皆能通過。

## 貢獻者指南 (Guide for Contributors)

我們仰賴測試來確保：
1.  **程式碼正確性**：您新增的功能（如 `scripts/` 中的新工具）能如預期般運作。
2.  **模型相容性**：您提交的新模型或修改，與現有的資料格式 (`docs/data-formats.md`) 和推論流程相容。
3.  **防止迴歸 (Regression)**：您的修改沒有破壞任何現有功能。

## 目錄結構

測試腳本應依照其測試的「對象」或「類型」進行組織：
```
tests/
│ ├── test_data_utils.py # (範例：測試 data_preprocessing 相關功能的單元測試)
│ ├── test_model_loader.py # (範例：測試模型載入與推論介面的單元測試)
│ ├── test_integration_flow.py # (範例：整合測試，模擬從資料輸入到模型輸出的完整流程)
│ └── fixtures/ # 存放測試所需的模擬資料或小型模型檔案
└── sample_input.json
```
## 如何執行測試

本專案使用 [請填入您使用的測試框架，例如：pytest, unittest] 進行測試。

1.  **安裝測試依賴**：
    在提交貢獻前，請確保您已安裝所有開發與測試所需的依賴庫（可能在 `requirements-dev.txt` 中）：
    ```bash
    pip install -r requirements-dev.txt
    # (或是您指定的 pytest/unittest 安裝指令)
    ```

2.  **執行所有測試**：
    在專案根目錄下，執行以下指令以運行所有測試：

    ```bash
    # (如果使用 pytest)
    pytest tests/
    
    # (如果使用 Python 內建的 unittest)
    python -m unittest discover tests/
    ```

3.  **執行特定測試**：
    若您只想針對您修改的部分進行測試：
    ```bash
    # (範例：僅執行 pytest 的 test_data_utils.py)
    pytest tests/test_data_utils.py
    ```

## 新增測試

當您提交新的功能或修復錯誤 (Bug) 時，請一併提交對應的測試案例：

* **新功能 (New Feature)**：請新增測試來驗證新功能的正確性。
* **錯誤修復 (Bug Fix)**：請新增一個「會重現該錯誤」的測試案例（確保在修復前它會失敗），並驗證您的修復能讓此測試通過。

---

**感謝您的貢獻！**

完善的測試是維持專案品質的基石。如果您對如何撰寫測試有疑問，請參考現有的測試腳本，或在您的 Pull Request 中提出討論。
