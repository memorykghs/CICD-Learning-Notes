# 0 - CI / CD Pipeline Introduction
## What is a CI / CD pipeline?
> This is a simpel introduciton.

CI / CD 的目的就是將軟體的交付過程自動化，包含 builds code、run test、自動化部署新版本等等。CI / CD pipeline 減少了人為錯誤，並提供一些 feedback 給開發人員，讓產品快速迭代。

CI / CD pipeline 在整個軟體產品的生命週期中引入了自動化過程以及持續監控，包括**集成 ( Integration )**、**測試階段 ( Test Phrase )**到**交付 ( Delivery )**和**部署( Deployment )**。

實際上 CI 和 CD 應該要拆成兩個部分來看，比較常見的情境是開發人員執行 git push 到 Gitlab，將程式更新至 server 的步驟交由 Jenkins 負責。

![](/images/0-1.png)
[圖片來源](https://www.analyticsvidhya.com/blog/2021/07/a-step-by-step-guide-to-create-a-ci-cd-pipeline-with-aws-services/)

#### Contiuous Intgration ( CI ) 持續整合
軟體的開發流程可大致分為程式建置及程式測試。

* **程式建置**
開發人員在每一次的 commit & push 之後，都能夠於統一的環境自動 build 程式，避免因本機環境和套件版本不同造成的 service 異常。

* **程式測試**
程式編譯完成後會透過「單元測試」來測試新功能是否正確，以及是否影響到現有功能。

#### Continuous Delivery
是一種軟體工程方法，確保團隊在較短週期內開發的產品可以隨時輕鬆發佈。

#### Contiunous Deploment ( CD ) 持續部署
透過自動化的方式，將寫好得程式碼更新到機器上並公開對外服務，也會透過監控確保相關服務如資料庫等，等檢查服務是否存活。
<br/>

![](/images/0-2.png)
[圖片來源](https://www.cyberark.com/zh-hant/what-is/ci-cd-pipeline/)

## CI / CD 工具介紹
| 名稱 | 類型 |
| --- | --- |
| GitLab CI | 版控工具 |
| GitHub | 版控工具 |
| Jenkins | 自動化建置工具 |
| Drone CI | 自動化建置工具 |
| Circle CI | 自動化建置工具 |
| AWS CodePipeline | |
| Docker | 迅速佈署環境工具 |
| K8S | 管理 Docker Container 工具 |
| Helm | 快速建置各環境 K8S 工具 |
| Grafana | 機器數據監控工具 |
| ELK | Log 蒐集工具 |
| Telegram | 通訊、錯誤通知工具 |
| Slack | 通訊、錯誤通知工具 |

## 大綱
1. Stages of a CI/CD pipeline
2. Example of CI/CD Pipeline
3. CI/CD pipeline Best Practices
4. Advantages of CI/CD pipelines
5. Important CI/CD tools
6. Why Does the CI/CD Pipeline Matter for IT Leaders?
7. Ci/CD Pipeline KPI

## 參考
* https://www.guru99.com/ci-cd-pipeline.html
* https://ithelp.ithome.com.tw/articles/10219083
* https://vocus.cc/article/620e7e17fd897800015b164d
