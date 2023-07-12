# SF_C2.7
0. Разверните Prometheus Stack через docker-compose, в котором будет:
-
-Prometheus;
-Grafana;
-Node Exporter;
-Blackbox Exporter;
-AlertManager.
0. Соберите метрики с https://lms.skillfactory.ru через Blackbox, соберите метрики с вашего сервера через Node Exporter.

0. Создайте dashboard в Grafana, в котором будут отображены следующие метрики:

-На вашем сервере (или локальной машине):

-время работы (Uptime);
-нагрузка на процессор (CPU) в %;
-использование памяти (RAM) в %;
-использование диска в %.
-На lms.skillfactory.ru:

-возвращаемый статус-код;
-задержка ответа сайта;
-срок действия сертификата.
0. Добавьте алерты в AlertManager на следующие события:

-изменился статус-код сайта lms.skillfactory.ru;
-задержка превышает 5 секунд lms.skillfactory.ru;
-сервер перезагрузился (через метрику Uptime).