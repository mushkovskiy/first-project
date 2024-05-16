# Шпаргалка markdown

## Выделение текста

Вы можете выделять текст в markdown с помощью символов `_` или `*`. Например:

Пример _курсива_ и **жирного** текста.

## Заголовки

Заголовки можно создавать с помощью символа `#`. Чем больше `#`, тем меньше заголовок. Например:

# Заголовок первого уровня

## Заголовок второго уровня

### Заголовок третьего уровня

## Выделение кода

Чтобы выделить текст как код, поместите его в тройные кавычки `````.

```
mkdir my_project
cd my_project
git init
```

Это лишь некоторые функции markdown.

# Шпаргалка по GIT

## Как исправить коммит

1. Дополнить коммит новыми файлами или новыми изменениями, добавить файл с изменениями или новые файлы в индекс, после выполнить — git commit --amend --no-edit

2. Изменить сообщение коммита — git commit --amend -m 'Новое сообщение...'
   Выход из редактора nano - ctrl+x
   Выход из редактора Vim - esc -> :qa! -> enter

3. Как откатиться назад, если «всё сломалось»

3.1 Выполнить unstage изменений — git restore --staged <file>

3.2 Чтобы «сбросить» все файлы из staged обратно в untracked/modified git restore --staged .

3.3 «Откатить» коммит — git reset --hard <commit hash>

3.4 «Откатить» изменения, которые не попали ни в staging, ни в коммит, — git restore <file>
Изменения в файле «откатятся» до последней версии, которая была сохранена через git commit или git add.

4. Просматриваем изменения в файлах

4.1 git diff - Эта команда сравнит последнюю закоммиченную версию файла c текущей (modifed)
Команда git diff сравнит последнюю закоммиченную версию файла с той, что находится в состоянии modified.

4.2 Просматриваем изменения в staging area - git diff --staged
Команда git diff --staged покажет изменения в staged-файлах относительно последних закоммиченных версий.

4.3 git diff <commit hash A> <commit hash B> - сравнение двух коммитов
