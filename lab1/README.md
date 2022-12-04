### Цель работы 
Запустить приложение при помощи ansible, научиться писать плейбуки и пользоваться group vars.  

Docker-образ: https://hub.docker.com/repository/docker/timurbabs/django

### Рекомендуемая документация

- [Инфраструктура как код #1: понятие инфраструктурного кода (Лекция)](https://www.youtube.com/watch?v=RS9fAJM0tf0&ab_channel=DeusOps)
- [Инфраструктура как код #2: Знакомство с Ansible (Лекция)](https://youtu.be/GFL6-DlSQH0)
- [Как поднимать виртуальные машины в Vagrant](https://www.youtube.com/watch?v=dgm5MtCcIMs&t=5150s)
- [Документация Ansible](https://docs.ansible.com/ansible/latest/user_guide/index.html#writing-tasks-plays-and-playbooks)
- [Подборка по Ansible](https://gitlab.com/deusops/lessons/documentation/ansible)

### Задания на работу  
- Установить Ansible используя [гайд по установке](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)  
- Установить [Vagrant](https://developer.hashicorp.com/vagrant/downloads)  
- Поднять Vagrant хост при помощи файла Vagrantfile используя команду [*vagrant up](https://drive.google.com/drive/u/0/folders/1Ev8N8LijxNR2npEwhoUFlxBuznf--ujP)
- Написать `inventory`-файл для развернутых хостов  
- Написать плейбук для установки Docker  
- Клонировать [репо](https://github.com/mdn/django-locallibrary-tutorial) на ноды группы `app`   
- Запустить приложение на нодах группы `app` используя ansible
