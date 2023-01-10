
http://0.0.0.0:3000/metrics Посмотреть метрики из пода curl

например метрика
app_bin_send_request_count метрика

заходим и вставляем название метрики. дальше в фигурных скобка перечисляем фильтрацию поле=значение
app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"}


{namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"} - поля фильтрации

кол-во запросов меркури
sum by (namespace)(rate (app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*"}[1m]))
кол-про продаж 
sum by (namespace)(rate (app_bin_send_request_count {namespace=~"prod-mercury",pod=~"prod-transaction-manager.*",request=~"endSale", sign=~"0"}[1m]))