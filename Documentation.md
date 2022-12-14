# Документация

Ресурпак эксклюзивно разработан для сервера в майнкрафт.. но без дополнительных рп он не полон.

## Скачивание

[Скачать](https://github.com/mrf0rtuna4/HeypersRP/releases/tag/HRP.beta.2.19)

## Альтернативное скачивание

Итак для того чтобы скачать ресурспак по крутому вам нужно октыть консоль(Win+R,cmd) и пишем

```cd (путь к папке с ресурспаками)
git clone https://github.com/mrf0rtuna4/HeypersRP.git
```

Ждем скачивания и ваш ресурспак установлен.

## Скачивание и получение каждого коммита без повторного клона и поддержка репо

1. Нужно форкнуть репозиторий на github (кнопка fork) в свой профиль.

2. Клонируем репозиторий к себе на компьютер из своего профиля:

```cd /var/projects
git clone https://github.com/user/repo.git repo
```

3.Привязываем оригинальный репозиторий к своему.

Только что склонированный репозиторий имеет только одну привязку к удалённому репозиторию. Она называется origin и указывает на вашу копию на GitHub (ваш профиль), а не на оригинальный репозиторий. Чтобы иметь привязку и к оригинальному репозитоирию, нужно добавить ещё одни привязку, назовём её upstream:

```cd repo
git remote add upstream git://github.com/origin-name/repo.git
git fetch upstream
```

Теперь мы можем полноценно работать с репозиторием, как вливать, так и забирать всё что в репо есть.
Вот так можно обновится с оригинального репозитория:

```git checkout master
git pull upstream master
git merge upstream/master
```

4.Вносим правки в код. Можно вносить изменения в файлы и коммитить их. Можно прямо в master, но, лучше для каждой фичи создавать отдельную ветвь:

```cd repo
git checkout -b master_feature #создаём новую ветвь и переключаемся на неё
git add filename
git commit -m 'implement mega feature'
git push origin master_feature  #загружает изменения из текущей локальной ветви в origin ветвь
```

5.Создаём ПР. Заходим на github на страницу оригинального репозитория. Создам Pull Request на основе созданной нами ветви. Обычно github уже видит созданную ветвь, которая не смерджена с мастером, и сам предлагает создать PR к ней.

После создания ПР ваши изменения будут видны всем пользователям. После проверки ПР, изменения могут быть вмерджены авторами (точнее сказать не авторами, а теми, кто имеет право на запись — push). Или же могут быть запрошены корректировки кода, которые потребуют дополнительных комментариев или даже новых коммитов от вас.
