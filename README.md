# Визуализация нематериальных активов

Аккумулирование исследовательских данных с дальнейшим анализом и возможностью построения графиков в разных категориях. Поиск инсайтов.

## Инструкция по установке

Данная инструкция дает возможность установить локальную копию Платформы для тестирования и разработки. По выгрузке не рабочий сервер смотрите Deployment.

### Обсуждение

Прежде чем принимать решения об обсуждении проблемы, попробуйте обновить Docker до последней версии и проверьте не исправило ли это вашу проблему. Ознакомьтесь c [инструкцией по установке и обновлению Docker](https://docs.docker.com/installation)

```
$ sudo apt-get update

```

### Установка

Автоматические сборки данного образа доступна через хаб [Dockerhub](https://hub.docker.com) и являются рекомендованным способом установки

Say what the step will be

```
docker pull hanebauer/rebrain-devops-task-checkout
```

Можно собрать образ самостоятельно

```
docker build -t hanebauer/rebrain-devops-task-checkout github.com/hanebauer/rebrain-devops-task-checkout
```

End with an example of getting some data out of the system or using it for a little demo

## Быстрый старт

Для запуска просто запустите команду:

```
docker run --name platform -itd --restart always \
  --publish 1432:1432 \
  --volume /srv/docker/platform:/var/lib/platform \
  hanebauer/rebrain-devops-task-checkout
```

## Deployment

1. Download the updated Docker image:

```
docker pull hanebauer/rebrain-devops-task-checkout
```
2. Stop the currently running image:

```
docker stop platform
```
3. Remove the stopped container

```
docker rm -v platform
```
4. Start the updated image

```
docker run --name platform -itd --restart always \
  --publish 1432:1432 \
  --volume /srv/docker/platform:/var/lib/platform \
  hanebauer/rebrain-devops-task-checkout
```

## Authors

* **Maxim Rozhkov** - *Initial work* - [Hanebauer](https://github.com/hanebauer)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

