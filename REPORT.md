# Отчёт по мидтерму: Инфраструктурный репозиторий

Репозиторий: https://github.com/kasymovaz-ui/infra-project

## Блок 1. Основы

### 1.1 Настройка и первый коммит
Команды и вывод: git config, git clone, git commit, git push, git log --oneline.
Пояснение: первый коммит содержит только .gitignore.

### 1.2 Файлы проекта
Команды и вывод: git status (без .env и app.log), три коммита, git push, git log --oneline.
Пояснение: ...

### 1.3 Просмотр изменений
Вывод git diff до git add, git diff и git diff --staged после него.
Пояснение: второй git diff пустой, потому что он сравнивает рабочую папку с индексом, а после git add изменение уже в индексе. git diff --staged сравнивает индекс с последним коммитом, поэтому показывает изменение.

## Блок 2. История и ветки

### 2.1 История
Вывод: git log --oneline, git log --oneline --graph --all, git show HEAD~1.
Пояснение: HEAD~1 соответствует коммиту b269683 feat(ansible): add inventory, config and playbook.

### 2.2 Ветка и слияние
Вывод git merge (Fast-forward), git branch.

### 2.3 Конфликт
Содержимое all.yml с маркерами, итоговый файл, git log --oneline --graph.

## Блок 3. Удалённый репозиторий и MR

### 3.1 git pull
Вывод git pull и git log --oneline.

### 3.2 Merge Request
Ссылка: https://github.com/kasymovaz-ui/infra-project/pull/1
Команды, описание MR, сообщение коммита.

### 3.3 Уборка веток
Вывод git push origin --delete (ветка уже удалена GitHub автоматически), git fetch --prune, git branch -a.

## Блок 4. Docker
Последние строки docker build, вывод curl, ссылка на MR: https://github.com/kasymovaz-ui/infra-project/pull/2

## Блок 5. Исправление ошибок

### 5.1 restore и amend
Команды git restore docker/Dockerfile и git commit --amend -m "docs: update readme", вывод git log.

### 5.2 revert
Команды и вывод git revert 38c6a8f.
Пояснение: коммит уже опубликован, и его удаление из истории потребовало бы force-push, из-за чего у других история разошлась бы с серверной. git revert добавляет новый коммит-отмену и не переписывает историю.

## Контрольные вопросы
1. Что такое коммит и зачем нужна область индекса?
2. Что такое ветка в Git?
3. Что такое HEAD?
4. Чем git fetch отличается от git pull?
5. Почему .env нельзя добавлять в репозиторий?
