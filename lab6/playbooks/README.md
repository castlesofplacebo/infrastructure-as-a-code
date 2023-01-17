## Цель работы

Научиться настраивать мониторинг для серверных приложений

[Рекомендуемое приложение для мониторинга](https://github.com/grafana/spring-boot-demo) (можете выбрать своё, например, разработанное на предыдущих курсах. Но все возникающие специфичные вопросы ложатся на вас)

## TODO:
1. Prometheus Role - compare with https://github.com/cloudalchemy/ansible-prometheus  
add_source when runs several times
2. Grafana Role - compare with https://github.com/cloudalchemy/ansible-grafana  
Add more flexibility
add_dashboards when runs several times
3. Loki Role  
Add Promtail

## Рекомендуемая документация

- [Как поднимать виртуальные машины в Vagrant](https://gitlab.com/deusops/lessons/documentation/vagrant)
- [Документация Prometheus, Grafana и Loki](https://gitlab.com/deusops/lessons/documentation/prometheus-grafana)
- [Подборка информации по Ansible и написанию ролей](https://gitlab.com/deusops/lessons/documentation/ansible)

## Ход работы

1. Развернуть виртуальную машину для приложения (app) и виртуальную машину для будущей системы мониторинга (monitoring) через Vagrant-file
2. Написать Ansible Playbook для развертывания системы мониторинга и приложения
3. Через molecule разработать отдельные Ansible-роли для развертывания Grafana, Prometheus, Loki, Docker и пр. Использовать Galaxy для хранения ролей, роли должны проходить стандартные “molecule test”
4. Установить на monitoring сервисы Grafana, Prometheus и Loki
5. Установить на app само приложение и настроить сбор метрик из app /actuator/prometheus
6. Разработать шаблоны для конфигурационных файлов поднимаемых сервисов
7. Добавить в шаблоны дашборды графаны и визуализировать метрики
8. **Добавить в шаблоны алертинг в виде письма на почту**