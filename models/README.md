# BlueTooth6.0 Models

歡迎來到本專案的模型儲存區。

本目錄 (`models/`) 存放了所有已訓練完成、可供部署的模型檔案，以及各模型的具體說明文件。

## 模型概覽

本平台提供的模型旨在解決 [請簡述模型的核心應用領域，例如：室內定位、場域辨識等] 相關問題。所有模型皆已根據 `docs/` 目錄中定義的 [**標準資料格式**](../docs/data-formats.md) 進行訓練與驗證。

## 目錄結構

本儲存區依據模型的類型或功能進行分類，結構如下：
```
models/ 
├── indoor-positioning/ # 範例：室內定位模型 
├── model_v1.h5
│   └── README.md # 說明此模型的具體資訊 (準確率、輸入/輸出等)
├── area-classification/ # 範例：場域分類模型
├── model_a.onnx
│   └── README.md # 說明此模型的具體資訊
└── ... # 其他模型類別
```

## 如何使用模型

1.  **選擇模型**：請瀏覽上述目錄，或參考下方的「模型清單」，找到符合您應用需求的模型。
2.  **查閱文件**：點擊進入特定模型的子目錄（例如 `indoor-positioning/`），詳閱其 `README.md`，以了解該模型的：
    * 效能指標（如準確率、延遲）
    * 詳細的輸入/輸出格式（範例：輸入 RSSI 向量，輸出 [x, y] 座標）
    * 適用的應用場景與限制
3.  **下載與部署**：下載模型檔案（例如 `.h5`, `.onnx`, 或 `.pt` 檔案）。
4.  **整合應用**：參考根目錄 `docs/` 下的 [**部署教學**](../docs/deployment.md) 文件，將模型整合至您的應用程式或服務中。

## 模型清單 (Model Inventory)

* **[室內定位模型 (Indoor Positioning)](./indoor-positioning/README.md)**
    * **簡介**：[簡要說明，例如：基於 BLE RSSI 訓練，用於預估裝置的二維座標]
    * **檔案**：`model_v1.h5`

* **[場域分類模型 (Area Classification)](./area-classification/README.md)**
    * **簡介**：[簡要說明，例如：基於 IQ 資料訓練，用於辨識裝置所在的場域類型（如：會議室、走廊）]
    * **檔案**：`model_a.onnx`

* *...（請依實際釋出模型陸續新增）...*

---

**技術支援**

如果您在模型使用或部署上遇到問題，請優先查閱 [**使用者導覽**](../docs/getting-started.md)。若問題未解，歡迎透過 [Issues](https://github.com/[Your-Organization]/[Your-Repo]/issues) 回報問題。
