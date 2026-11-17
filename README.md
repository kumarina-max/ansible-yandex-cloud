# Ansible — настройка виртуальной машины

## Описание

Репозиторий содержит Ansible-playbook для автоматической установки и настройки Docker на виртуальной машине в Yandex Cloud.

## Структура проекта

```text
ansible-yandex-cloud/
├── inventory/
│   └── hosts.ini
├── playbooks/
│   └── install-docker.yml
└── README.md
```

## Что делает playbook

Файл `playbooks/install-docker.yml` выполняет:

- установку Docker Engine;
- установку Docker Buildx и Docker Compose Plugin;
- настройку и запуск службы Docker;
- добавление пользователя `ubuntu` в группу `docker`;
- проверку установки.

## Запуск

Для применения конфигурации используется команда:

```bash
ansible-playbook -i inventory/hosts.ini playbooks/install-docker.yml
```

Для подключения необходим SSH-доступ к виртуальной машине.

## Связанные проекты

- [Terraform — облачная инфраструктура](https://github.com/kumarina-max/terraform-yandex-cloud)
- [Docker и CI/CD — веб-приложение](https://github.com/kumarina-max/docker-app-yandex-cloud)
- [Docker Hub — опубликованный образ](https://hub.docker.com/r/kumarina/docker-app-yandex-cloud)
