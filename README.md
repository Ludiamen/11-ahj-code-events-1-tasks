[![Build status](https://ci.appveyor.com/api/projects/status/72uxrosjq55gsdxr?svg=true)](https://ci.appveyor.com/project/Ludiamen/11-ahj-code-dom)

[Сcылка на GitHub Pages](https://ludiamen.github.io/11-ahj-code-dom/)

Правила сдачи задания:

1. **Важно**: в рамках этого ДЗ нужно использовать менеджер пакетов yarn. Это значит, что никакого `package-lock.json` в репозитории быть не должно.
1. **Важно**: всё, включая картинки и стили, должно собираться через Webpack и выкладываться на GitHub Pages через AppVeyor.
1. В README.md должен быть размещён бейджик сборки и ссылка на GitHub Pages.
1. В качестве результата пришлите проверяющему ссылки на ваши GitHub-проекты.

---

### TOP Tasks

#### Легенда

Вы разрабатываете трекер задач, в котором есть возможность отображать назначенные пользователю задачи. Выглядеть это должно примерно так:

![](./pic/tasks.png)

Проектировщики и заказчик приложения решили, что пользователь может фильтровать и добавлять задачи с помощью поля ввода. Некоторые задачи можно закреплять (pin).

#### Описание

1. Добавлять задачи можно при следующих условиях: в поле ввода есть текст, и пользователь нажал Enter. Если текста нет, но пользователь всё равно нажал Enter, должно выводиться сообщение об ошибке. Предложите, как это можно сделать, только ни в коем случае не alert и не console.
1. Задача добавляется в блок All Tasks, а поле ввода очищается.
1. Когда закреплённых задач нет, в блоке Pinned должно отображаться No pinned tasks.
1. Когда закреплённые задачи есть, они отображаются в блоке Pinned и не участвуют в процедуре фильтрации:
    * их отображение никак не зависит от состояния фильтра,
    * они не отображаются в блоке All Tasks.
1. При пустом поле ввода в блоке All Tasks отображаются все задачи с учётом условий предыдущего пункта (т. е. все, кроме Pinned).
1. При изменении поля ввода содержимое блока All Tasks автоматически пересчитывается: отображаются только те задачи, название которых начинается с того, что введено в поле ввода, без учёта регистра.
1. Если значению поля ввода не удовлетворяет ни одна из задач, то в блоке All Tasks отображается No tasks found.
1. При выставлении переключателя (круглая иконка справа) задача из блока All Tasks попадает в Pinned.
1. При снятии переключателя (круглая иконка справа) задача из блока Pinned попадает в блок All Tasks. При этом учитывайте состояние фильтра.

Все задачи должны храниться в едином массиве в памяти JS. Каждая задача должна из себя представлять объект класса Task, который вы разработаете сами. Перестройка DOM-дерева должна происходить на основании объектов, хранящихся в памяти.

Всё должно собираться через Webpack и выкладываться на GitHub Pages через CI.

**В качестве результата пришлите проверяющему ссылку на ваш GitHub-проект. Не забудьте установить бейджик сборки.**