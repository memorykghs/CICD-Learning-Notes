# 01 - GitLab 環境安裝
* 官方提供 [gitLab image](https://hub.docker.com/r/gitlab/gitlab-ee/)

* 圈內大神 [ Sameer Naik 的 github](https://github.com/sameersbn/docker-gitlab)

* 官網[安裝說明](https://docs.gitlab.com/ee/install/docker.html)

## Install GitLab
1. 可以在網站上確認要拉的 gitLab image 版本及內容。
    ![](/images/gitlab/1-1.png)

    pull image 到本地。
    ```docker
    docker pull gitlab/gitlab-ee
    ```

    檢查 image 是否被拉下來了。
    ```docker
    docker images
    ```
    ![](/images/gitlab/1-2.png)
<br/>

2. 執行 container。
    ```docker
    docker run -d -name gitlab -p 8080:80 gitlab/gitlab-ee
    ```
    有人會加上 `--restart always` 讓 gitLab 在電腦開機時重啟。
    ![](/images/gitlab/1-3.png)

    查看 container 是否有正常運作。
    ```docker
    docker ps
    ```
<br/>

3. 先去 GitLab 官網上註冊，然後在網頁上輸入下面的網址查看 GitLab 頁面。
    ```
    http://localhost:8080
    ```
    ![](/images/gitlab/1-4.png)

    如果網頁出現 `502` 的話，多重新整理幾次應該就可以了。沒帳號就註冊之後登入即可。

## Q & A
> 1. 不知道為什麼登入的時候一直被擋在門外QQ

 ![](/images/gitlab/1-5.png)

## 參考
* https://medium.com/phelps-laboratory/docker-install-gitlab-52ea641eca90
* https://ithelp.ithome.com.tw/articles/10211148