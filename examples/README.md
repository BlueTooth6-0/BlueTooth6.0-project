# 範例程式碼 (Examples)

歡迎使用本專案的範例程式碼庫。

本目錄 (`examples/`) 提供了多種情境下的範例腳本，旨在協助開發者快速理解如何載入 `models/` 目錄中的模型，並整合 `scripts/` 中的工具，以執行具體的應用任務。

## 目錄結構

本目錄下的範例程式碼依照其主要功能或應用情境進行分類：
```
examples/
├── data_preprocessing/ # 資料前處理範例
│   └── preprocess_rssi.py # (範例：如何將原始 RSSI 轉換為模型輸入格式)
├── model_inference/ # 模型推論範例│ ├── run_positioning.py # (範例：載入室內定位模型並進行預測)
│   └── run_classification.py # (範例：載入場域分類模型進行預測)│ ├── visualization/ # 結果視覺化範例
│   └── plot_location.py # (範例：將模型的座標輸出繪製在地圖上)
└── ... # 其他範例情境
```
## 如何執行範例

所有範例均建議在已設置好依賴的環境中執行。

1.  **環境設置**：
    請先確保您已依照根目錄 `README.md` 或 `docs/getting-started.md` 中的說明，完成所有必要的環境安裝與依賴庫配置。

2.  **準備資料**：
    部分範例可能需要範例資料集。請檢查該範例腳本開頭的說明，或 `docs/data-formats.md` 以準備正確格式的輸入資料。

3.  **執行腳本**：
    開啟您的終端機 (Terminal)，切換至本專案根目錄，然後執行您感興趣的範例。

    例如，執行室內定位模型的推論範例：
    ```bash
    # (此為範例指令，請依實際腳本設計修改)
    python examples/model_inference/run_positioning.py --model_path models/indoor-positioning/model_v1.h5 --input_data path/to/your/data.csv
    ```

## 範例清單

* **[資料前處理](./data_preprocessing/)**:
    * `preprocess_rssi.py`: 展示如何讀取原始 BLE RSSI 資料，並依照 `docs/data-formats.md` 規範進行清理、標準化，轉換為模型可接受的向量格式。

* **[模型推論](./model_inference/)**:
    * `run_positioning.py`: 載入一個已訓練的「室內定位模型」，接收符合格式的輸入，並印出預測的 (x, y) 座標。
    * `run_classification.py`: 載入一個已訓練的「場域分類模型」，接收符合格式的輸入，並印出預測的場域標籤。

* **[結果視覺化](./visualization/)**:
    * `plot_location.py`: (範例) 讀取 `run_positioning.py` 的輸出結果，並使用 matplotlib 或其他庫將預測的座標點繪製在示意圖上。

---

**需要協助？**

如果您在執行範例時遇到困難，請參閱 `docs/` 目錄下的詳細文件。若仍無法解決，歡迎透過 [Issues](https://github.com/[Your-Organization]/[Your-Repo]/issues) 提問。
