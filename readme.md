# Learn kubernetes yaml - K8s

先去安裝 Docker Desktop 裡頭設定可以直接安裝 K8s

啟用
```
kubectl apply -f ./
```

關閉
```
kubectl delete svc --all & kubectl delete deploy --all
```
---
# 開速編輯 yaml 檔
使用 `vscode-plugin:cloud-code`
可以使用`cloud-code` 範例學習

with vscode `shift + commamd + P`
```
> Cloud Code:New Application 
```
裡面有多種語言範例架構學習

---
首先有一個 前端/後端/資料庫 的一個基本的伺服器架構
將其三個架構封裝成`Image`
```
Docker build -it <ImageName> <PATH>
```
如果要使用本地的Image 要記得在 deployment.yaml 的 template.spec
加上 `imagePullPolicy: Never` 預設我有將此行隱藏

> 此專案為個人學習註解使用持續編輯中