# CV

Проект для формирования PDF-файла резюме из Tex-файла.

## Для работы нужно

1. Установить дистрибутив LaTeX, включающий в себя компилятор xelatex.

    Например, `Tex Live` - это полный дистрибутив весом 5 Гб со всеми пакетами и библиотеками.

    В том числе tlmgr (менеджер пакетов) и biber (списки публикаций).

2. В VSCode добавить расширение `latex-workshop`.

3. В настройки VSCode в `settings.json` добавить блоки:
``` json
"latex-workshop.latex.tools":
[
    {
        "name": "xelatex",
        "command": "xelatex",
        "args":
        [
            "-interaction=nonstopmode",
            "-synctex=1",
            "%DOC%"
        ]
    },
    {
        "name": "biber",
        "command": "biber",
        "args":
        [
            "%DOCFILE%"
        ]
    }
],

"latex-workshop.latex.recipes":
[
    {
        "name": "xelatex → biber → xelatex ×2",
        "tools":
        [
            "xelatex",
            "biber",
            "xelatex",
            "xelatex"
        ]
    }
]

```
