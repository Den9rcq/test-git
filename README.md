# Practical Git

`git remote -v` - показывает [rep_link]

## Связка репозитория с GitHub
1. `git status` - показывает изменённые файлы
2. `git add .` - добавляет все файлы в stage
3. `git commit -m "комментарий"` - создаёт commit
4. `git log / git log --oneline` - показывает commits/commit
5. `git push [rep_link] [branch_name]` - заливает изменения на GitHub
6. `git pull [rep_link] [branch_name]` - забирает изменения из GitHub

## Команды для удаления и отката
1. `git reset` - удаляет файл из stage
2. `git reset --hard` - возвращает проект к последнему commit
3. `git diff [name_file]` - показывает все изменения в проекте, файле)

## Команды для создания и слияния веток
1. `git branch [name_branch]` - показывает, создаёт ветку 
2. `git branch -d [name_branch]` - удаляет ветку
3. `git checkout [name_branch]` - переходит на ветку
4. `git checkout -b [name_branch]` - создаёт и сразу переключается на эту ветку
5. `git merge [name_branch]` - сливает ветки. Выполняем из ветки, в которую хотим сделать слияние. [name_branch] - чей код мы хотим перенести в основную ветку

### GitFlow
1. Создание репозитория и клонировать его себе на компьютер.
2. Создать ветку разработки develop от главной ветки (master, main).
3. Создать от ветки develop **feature/**-ветки и мержить **feature**-ветки в develop, когда фичи будут выполнен.
4. Создание ветки release/0.1.0 от develop.
5. Когда ветка release/0.1.0 закончена, то она мержится в develop и main, затем удаляется.
6. Если в ветке main обнаруживается ошибка, то создаётся hotfix-ветка.
7. Когда работа над hotfix-веткой завершается, то её нужно мержить в develop и main.
