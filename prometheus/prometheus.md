
curl http://0.0.0.0:3000/metrics Посмотреть метрики из пода curl

web
 curl http://localhost:8081/actuator/metrics

 


{namespace=~"tifa-boards"} 

например метрика
app_bin_send_request_count метрика

заходим и вставляем название метрики. дальше в фигурных скобка перечисляем фильтрацию поле=значение
app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"}


{namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"} - поля фильтрации

кол-во запросов меркури
sum by (namespace)(rate (app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"}[1m]))
кол-про продаж 
sum by (namespace)(rate (app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*",request=~"endSale", sign=~"0"}[1m]))

новое имя подов

{namespace=~"tfi-mercury",pod=~"tfi-merc-transaction-manager-5d875dcb5-mbgjr.*"}
{namespace=~"dev-ortax",pod=~"dev-ortax-address-standardization-.*"}
dev-ortax-address-standardization-

ssl монитор 
certificate_expiration_timestamp_seconds{namespace=~"prod-s8cps"} 

