# Шрифты для резюме

Подключаются отсюда, чтобы не зависеть от системных настроек.

Для подключений нужно знать внутреннее имя шрифта.

Его можно получить через утилиту `ttx` в **Linux**:

```
ttx -o - [шрифт.ttf] | grep -A 3 'nameID="1"'
```

В поле `nameID="1"` содержится имя шрифта, необходимое для подключения.