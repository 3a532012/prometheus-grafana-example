請依照順序執行namespace,configMap,serviceAccount,clusterRoleBind

後續再執行各exporter,promethues,grafana

原因：有依賴關係

為什麼不拆出來單獨一個folder?

因為這樣分比較爽

kubectl apply -f ./monitoring/namespace.yaml
kubectl apply -f ./monitoring/configMap.yaml
kubectl apply -f ./auth/serviceAccount.yaml
kubectl apply -f ./auth/clusterRoleBind.yaml


如果想更輕便的使用prometheus在k8s中，可以使用prometheus-operator
青菜蘿蔔各有所好，取決個人喜歡怎麼做

https://github.com/prometheus-operator/prometheus-operator