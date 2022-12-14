[&#8678; к содержанию](readme.md)

<span style="color:brown">Просмотр и удаление веток</span>
--
---
Просмотр полного списка веток можно сделать, используя параметр _**branch**_. Данная команда отобразит все существующие ветки, а также отметит текущую ветку звёздочкой **(*)** и выделит её цветом:

```bash
git branch
```

Также есть возможность вывести список всех удалённых веток с помощью флага _**-a**_:

```bash
git branch -a
```

Удаление ветки проводят добавлением флага _**-d**_ к парметру _**branch**_ c указанием имени ветки: 

```bash
git branch -d branch_name
```

Для принудительного удаления ветки используют флаг _**-D**_ с заглавной буквой. В данном случае ветка удаляется независимо от текущего статуса без каких-либо предупреждений:

```bash
git branch -D branch_name
```

Вышеотмеченные команды удаляют только локальную копию ветки, при этом она может сохраниться в удалённом репозитории. Для стирания удалённой ветки используют следующую команду:

```bash
git push origin --delete existing_branch_name
```

