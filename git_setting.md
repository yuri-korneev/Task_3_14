[&#8678; к содержанию](readme.md)

<span style="color:brown">Настройка Git</span>
--
---
После установки **Git** необходимо его настроить так, чтобы при создании коммита, указывался его автор.

Для этого необходимо открыть терминал (**Linux и MacOS**) или консоль (**Windows**) и ввести следующие команды:

```
#Установка имени пользователя
#Внутри кавычек указывается конкретное имя
git config --global user.name "<имя>"

#Затем устанавливается email
git config --global user.email "email адрес"
```