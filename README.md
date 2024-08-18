# Schedule Setup > Event Handing: POS and EXD device
work-portfolio(acti)

## 一、專案目的
1. **設定 POS 及 Extended Device 的事件觸發時間範圍**  
   此專案的主要目的是為了提供用戶能夠針對特定的 POS 和 Extended Device 設備設置事件觸發的時間範圍。事件可能包括如監視器端根據當前畫面狀態（ex: motion、tamper等）所觸發的特定資料格式。這些設置能夠讓系統在設定的時間範圍內，自動決定是否需要對事件進行反應（ex: 彈出視窗、發送電子郵件、啟動嗶聲警告或向手機發送通知等）。  
   - **事件**：監視器端會根據當前畫面送出特定的資料格式（ex: motion、tamper等）
   - **POS 及 Extended Device**：特定的攝影機類型

2. **增強用戶控制力**  
   通過讓用戶自定義觸發事件的時間範圍，這項功能不僅提升了系統的靈活性，也增加了用戶對設備管理的控制力。此功能適用於多種場景，例如用戶可以設定夜間自動觸發警報，而在工作時間內則只記錄而不觸發警報。

## 二、作業內容
1. **前端畫面呈現**  
   針對用戶界面進行了全面設計和實現，確保用戶能夠直觀地設置和管理 POS 及 Extended Device 的事件觸發時間範圍。前端頁面需具備良好的用戶體驗，並且支援多種設備的數據輸入與配置。
![image](https://github.com/user-attachments/assets/7153050d-9c19-44b0-ac22-2c9f293c4a98)


2. **事件觸發設定**  
   實現了具體的事件觸發邏輯，使得系統能夠在接收到攝影機的資料後，根據使用者設定的規則進行相應的操作。這部分涉及了對 ActiveX 和 API 的調用，確保數據能夠在不同模組間順暢傳遞。
   ![image](https://github.com/user-attachments/assets/658f5561-a006-43e9-af0d-dee481e6e5d4)


## 三、使用技術
1. **YUI.js 框架**  
   利用了 YUI.js 框架來構建和維護前端頁面。YUI.js 提供了豐富的 UI 元件和工具集，使得前端開發更加高效。

2. **Git 版本控制**  
   在開發過程中，使用了 Git 來進行版本控制，確保所有修改都能夠被追踪和回溯。這對於團隊協作尤為重要，能夠保證每個成員的貢獻都能夠被清晰記錄。

3. **ActiveX 資料串接**  
   通過 ActiveX 技術實現了與硬體設備的數據串接，確保系統能夠接收到來自不同設備的即時數據，並根據這些數據觸發相應的事件。

4. **API 資料串接**  
   使用了 RESTful API 來與後端進行通訊，確保前端設定的數據能夠正確傳送至後端並進行存儲和處理。

## 四、專案挑戰與解決方案
- **多設備兼容性**  
  POS 和 Extended Device 類型繁多且配置各異，為此專案必須確保系統能夠兼容多種設備，並能正確處理不同設備發出的事件。為了解決這個問題，我們設計了靈活的數據串接模組，通過抽象接口來統一不同設備的操作。

## 五、專案架構圖
<img width="807" alt="截圖 2024-08-16 清晨7 17 24" src="https://github.com/user-attachments/assets/b7618238-59b9-45ae-886c-6b5f9194905e">
