[&#8678; к содержанию](readme.md)

<span style="color:brown">Отмена произведенных изменений</span>
--
1. [Отмена неподготовленных измнений](#ref1)
2. [Отмена подготовленных изменений](#ref2)
3. [Отмена последнего коммита](#ref3)
4. [Изменение последнего коммита](#ref4)
---
<a id="ref1"></a>
## <span style="text-decoration: underline">Отмена неподготовленных изменений</span>

Восстановление файлов рабочего дерева, не подготовленных к коммиту, можно проводить с помощью параметра _**checkout**_, при этом указывается путь к файлу. Если этот путь не  указывать, то команда _**git checkout**_ изменит указатель **HEAD**, чтобы задать указанную ветку как текущую:

```bash
git checkout somefile.html
```

<a id="ref2"></a>
## <span style="text-decoration: underline">Отмена подготовленных изменений</span>

Для восстановления подготовленных файлов можно воспользователем параметром _**reset**_, при этом необходимо указать путь к файлу, чтобы убрать его из области подготовленных файлов. В это время откат изменений или модификаций происходить не будет, однако сам файл перейдёт в категорию не подготовленных к коммиту. Клманда выглядит следующим образом:

```bash
git reset HEAD anyfile.php
```

Если мы хотим сделать это действие для всех подготовленных файлов, путь к ним не указывается:

```bash
git reset HEAD
```
<a id="ref3"></a>
## <span style="text-decoration: underline">Отмена последнего коммита</span>

Откат последнего коммита производятс помощью параметра _**revert**_, при этом Создается новый коммит, содержащий обратные преобразования относительно предыдущего, и добавляется к истории текущей ветки:

```bash
git revert HEAD
```
<a id="ref4"></a>
## <span style="text-decoration: underline">Изменение последнего коммита</span>

Внести изменения в последний коммит можно с использованием параметра _**commit**_ с флагом _**--amend**_. _Пример ситуации_ - вы записали изменения, внесённые в ряд файлов, и потом поняли, что сделали ошибку в сообщении коммита. Для решения этой проблемы можно применить указанную команду, чтобы отредактировать сообщение предыдущего коммита, не изменяя его снимок:

```bash
git commit --amend -m "Updated message for the previous commit"
```

Также возможно вносить изменения в файлы, отправленные ранее. К примеру, вы изменили несколько файлов в ряде папок и хотите их записать как единый снимок, но забыли добавить в коммит одну из папок. Чтобы исправить такую ошибку, достаточно подготовить для фиксации остальные файлы и папки, и затем создать коммит с флагами _**--amend**_ и _**--no-edit**_.
