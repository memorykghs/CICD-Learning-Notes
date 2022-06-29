# 1 - Stages of a CICD pipeline
CI / CD pipeline 是一種為了因應任何開發人員交付新版本產品應執行步驟的**規範**。

它可以被分為幾個階段，每個階段失敗時都會透過像是 email、slack 或其他 通訊平台通知開發人員。以下是 CI / CD pipeline 的幾個重要階段：
![](/images/1-1.png)

## Source Stage 來源階段
在 Source Stage，CI / CD pipeline 由版控工具的 repository 觸發。程式碼的任何變更，都會觸發 CI / CD 工具的通知。其他常見的觸發包括 user-initiated workflows、automated schedules 和 其他管道的 results。

## Build Stage
CI / CD pipeline 的第二個階段，主要是 source code 還有與其相關的 dependency 的合併。最後將建立一個可以被執行的產品實例，這包產品最後應該要可以直接給使用者操作。

像是 C、C++、Java 或是 Go 等語言，是非手稿語言，需要先進行編譯，他們就是在此階段先被編譯。而像是 Python、JavaScript 和 Ruby 等不需要事先進行編譯，也就不需要此階段。

## Test Stage 測試階段
測試階段包括執行自動化測試，驗證軟體的功能與正確性。在此階段可以提高產品的正確性，防止一些容易重現的錯誤到達客戶端。

## Deploy Stage
這是產品上線的最後一個階段，一旦 build 成功通過所有的測試案例，就可以部署到正式的 server 上了。

## Example of CI / CD pipeline
* **Source Code Control** - 我們可以使用 GitHub 作為程式碼託管的私有儲存庫，幫助管理與集成應用程式相關的代碼。

* **Continuous integration** - 使用持續集成與交付的平台像是 CircleCI commit 。

* **Deploy code to UAT** - 設定 CircleCI，讓它可以將程式碼部署到
 AWS UAT server。

* **Deploy to production** - 重複 countinuous integration 步驟，將程式碼部署到 UAT。

## 參考
* https://www.cyberark.com/zh-hant/what-is/ci-cd-pipeline/