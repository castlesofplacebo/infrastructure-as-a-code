## Цель работы

Научиться писать Molecule-тесты для ролей

## ToDo:
1. Разобраться с комментариями

2. Добавить поддержку нескольких клиентов (через with)

3. Протестировать трафик в интернет через сервис OVPN (спойлер - сейчас не идет)

4. Возможность поднять сервер и клиент на отдельных тачках в молекуле + донастроить converge для локального тестирования через клиент openvpn (разобраться с сетевыми интерфейсами)

5. Настроить запуск роли на нескольких группах машин через груп варсы


## Рекомендуемая документация

- [Habr об OpenVPN](https://habr.com/ru/post/233971/)
- [VPN: ещё раз просто о сложном](https://habr.com/ru/post/534250/)
- [Урок из Школы DevOps: Тестирование ролей в Molecule](https://www.youtube.com/watch?v=0b3YXlffo1Q)
- [Статья про Molecule — тестируем роли Ansible](https://habr.com/ru/post/437216/)
- [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-ubuntu-20-04#step-6-generating-a-client-certificate-and-key-pair)

## Ход работы

1. Написать Ansible Playbook поднимающий OpenVPN сервер
2. Через Molecule инициировать структуру для роли и вынести задачи поднятия сервера, с конфигурацией через переменные
3. При завершении работы плейбук должен разместить в playbook-dir артефактный ovpn-файл для подключения
4. Роль должна проходить стандартные тестами molecule test
5. Плейбук подключает роль через ansible-galaxy