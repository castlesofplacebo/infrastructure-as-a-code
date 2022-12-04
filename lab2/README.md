## Цель работы

Научиться пользоваться Ansible Galaxy и писать роли

## Рекомендуемая документация

- [Инфраструктура как код #3: Ansible-роли и Galaxy](https://www.youtube.com/watch?v=sEzoDAfLstw)
- [Документация по Ansible Galaxy](https://docs.ansible.com/ansible/latest/galaxy/user_guide.html)

## Ход работы

1. Инициировать структуру роли “**Docker**” через Ansible-Galaxy
2. Вынести из предыдущего плейбука задачи установки Docker в отдельную роль
3. Параметризовать роль через переменные
4. Создать в gitlab группу для репозиториев с ролями, запушить роль “**Docker**” в репозиторий
5. Создать файл requirements.yml для установки роли Docker из репозитория
6. Запустить приложение на нодах группы `app` используя ansible-playbook с ролью “**Docker**”