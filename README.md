# 🐍 Thonny AI Helper 🤖

[![PyPI version](https://badge.fury.io/py/thonny-ai-helper.svg)](https://badge.fury.io/py/thonny-ai-helper)
[![Python Version](https://img.shields.io/pypi/pyversions/thonny-ai-helper.svg)](https://pypi.org/project/thonny-ai-helper/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

一個為 [Thonny IDE](https://thonny.org/) 設計的 AI 程式設計助手外掛 💡，旨在幫助您編寫、解釋和除錯程式碼。

![螢幕擷取畫面 2025-05-06 110739](https://github.com/user-attachments/assets/aa0b9af8-cbab-44ad-ab3e-7335c5065945)

## ✨ 功能特色

*   **💬 AI 對話視圖:** 在 Thonny 側邊欄提供一個專用的聊天視圖，您可以與 AI 進行對話。
*   **📜 歷史記錄:** 自動保存和載入您的對話記錄，方便回顧。
*   **✍️ Markdown 支援:** AI 的回應會以 Markdown 格式呈現，包含標題、列表、粗體、斜體和程式碼區塊。
*   **✂️ 程式碼區塊工具:**
    *   **複製按鈕:** 輕鬆複製 AI 提供的程式碼片段。
    *   **插入按鈕:** 將程式碼片段一鍵插入到您當前的編輯器中。
*   **🌐 OpenAI 相容:** 支援連接任何與 OpenAI API 相容的後端服務（例如本地執行的 Ollama 搭配 litellm，或商業服務）。
*   **🧩 編輯器整合:**
    *   在編輯器中選取程式碼，右鍵點擊「用 AI 助手解釋」，讓 AI 為您分析。
*   **셸 Shell 整合:**
    *   在 Shell 中選取輸出或程式碼，右鍵點擊「用 AI 助手解釋」，獲取解釋。
*   **⚙️ 彈性設定:** 在 Thonny 選項中設定您的 API URL、API Key 和選擇模型。
*   **🌍 多語言提示:** 自動提示 AI 使用您 Thonny 介面設定的語言（或作業系統預設語言）進行回應。

## 🚀 安裝

1.  開啟 Thonny IDE。
2.  前往 **工具 (Tools)** > **管理外掛 (Manage plug-ins...)**。
3.  在搜尋框中輸入 `thonny-ai-helper` 並按下 Enter。
4.  找到外掛後，點擊 **安裝 (Install)** 按鈕。
5.  安裝完成後，**重新啟動 Thonny** 🔄。

## 🛠️ 設定

安裝並重新啟動 Thonny 後，您需要進行設定才能使用：

1.  前往 **工具 (Tools)** > **選項 (Options...)**。
2.  切換到 **AI Assistant** 分頁。
3.  **API URL:** 輸入您的 OpenAI 相容 API 的基底 URL。
    *   格式通常是 `http://your-server-address:port/v1`。
    *   例如，如果您在本機使用 Ollama + LiteLLM，可能是 `http://localhost:8000/v1`。
4.  **API Key:** 輸入您的 API 金鑰（如果您的服務需要的話）。如果不需要，留空即可。
5.  **獲取模型:** 點擊 **獲取模型 (Fetch Models)** 按鈕。外掛會嘗試連接您提供的 API URL，抓取可用的模型列表。
6.  **選擇模型:** 從下拉選單中選擇您想要使用的 AI 模型。
7.  點擊 **確定 (OK)** 保存設定。

## 🎮 如何使用

1.  **開啟 AI 助手視圖:** 前往 **檢視 (View)** 選單，勾選 **AI Assistant**。您應該會在 Thonny 的側邊欄（預設在左側）看到一個新的面板。
2.  **開始對話:** 在視圖底部的輸入框中輸入您的問題或程式碼相關請求，然後點擊 **傳送 (Send)** 或按下 Enter。
3.  **等待回應:** AI 的回應會以 Markdown 格式顯示在對話區域。程式碼區塊下方會有「複製」和「插入」按鈕。
4.  **解釋程式碼 (編輯器):** 在 Thonny 的編輯器中選取一段程式碼，右鍵點擊，然後選擇 **用 AI 助手解釋 (Explain with AI Assistant)**。選取的程式碼會被發送給 AI 進行解釋，結果顯示在 AI 助手視圖中。
5.  **解釋程式碼 (Shell):** 在 Thonny 的 Shell 中選取文字，右鍵點擊，然後選擇 **用 AI 助手解釋 (Explain with AI Assistant)**。
6.  **清除對話:** 點擊 AI 助手視圖底部的 **清除 (Clear)** 按鈕可以清空當前的對話記錄。

## 🔧 依賴項

這個外掛需要以下 Python 函式庫：

*   `requests>=2.20.0`
*   `markdown-it-py>=3.0.0`

Thonny 的外掛管理器通常會自動處理這些依賴項的安裝。

## 📄 授權

本專案採用 MIT 授權。詳情請見 [LICENSE](LICENSE) 文件。

## 🙏 致謝與提醒

*   感謝 Thonny 開發團隊提供如此優秀且可擴展的 IDE。
*   請注意，AI 模型的回應可能不總是完全正確或安全的。請務必自行審查和測試 AI 產生的程式碼。
*   您的 API Key 和對話內容將會發送到您設定的 API URL。請確保您信任該服務提供商。

---

希望這個 AI 助手能幫助您更有效率地學習和編寫 Python！ 🎉 如果您遇到任何問題或有建議，歡迎提出 Issue。
