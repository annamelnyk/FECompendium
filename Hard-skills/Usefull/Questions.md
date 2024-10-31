# CI/CD & SCRUM & GIT
1. `merge` и `rebase`
  **merge:** - сохраняет полную историю и хронологический порядок (но история коммитов может быть заполнена (загрязнена) множеством коммитов)   
  **rebase:** - Rebase сжимает все изменения в один «патч».
    Затем он интегрирует патч в целевую ветку. В отличие от слияния, перемещение перезаписывает историю,
    потому что она передает завершенную работу из одной ветки в другую.
    В процессе устраняется нежелательная история. Очищает промежуточные коммиты, делая их одним коммитом.   
  **reset:** - откат коммитов
  `merge` и `rebase` - способ перенести изменения из одной ветки в другую. 
--------------------------------------------------------------
        

# HTML & CSS
1. Что нового появилось в  `HTML 5`?
  (В HTML5 появилось множество семантических элементов, а также тегов, позволяющих вставлять аудио и видео на сайт.
  <article> <aside> <audio> <canvas> <figcaption> <figure> <footer> <header> <hgroup>  <main> <menu> <nav> <output> <section> <time> <video>)
--------------------------------------------------------------

2.  Из чего состоит ширина блочного элемента?
  (width + padding + border + margin)
--------------------------------------------------------------

3. CSS Naming conventions (Соглашения об именованиях классов CSS)
(
  - BEM
  - SMACSS
  - ITCSS
  - OOCSS
  - AMCSS
)
**BEM:**
 - The block name should describe its purpose not what the element looks like nor how it behaves.
 Blocks can be nested in each other.
 You can have any number of nesting levels.

 - An element is a composite part of a block that can't be used separately from it. You can think of an element like a mother—child relationship.
The element name is separated from the block with a double underscore  
Elements can be nested inside each other.
You can have any number of nesting levels.
An element is always part of a block, not another element. This means that element names can't define a hierarchy such as block__elem1__elem2.

- A BEM modifier defines the appearance, state or behavior of a block element.

**OOCSS**
- OOCSS means Object-Oriented CSS and its purpose is to encourage code reuse and ultimately stylesheets that are easier to maintain.

OOCSS is centered around two main principles:

Separation of structure from skin
Separation of container and content
--------------------------------------------------------------

# JavaScript (ES6)
2. Pprototype
(* `Прототип` - это механизм, с помощью которого объекты JavaScript наследуют свойства друг от друга (от которого объект наследует методы и свойства). 
* ` [[Prototype]]` - скрытое свойство, которое либо равно `null`, либо ссылается на другой объект.
* `__proto__` - связь между экземпляром объекта и его прототипом. Позволяет задать прототип объекту.
* Свойство `__proto__` — исторически обусловленный геттер/сеттер для `[[Prototype]]`.
* `__proto__` - существует по историческим причинам, сейчас используется `Object.getPrototypeOf` и `Object.setPrototypeOf`
* Может быть только один `[[Prototype]]`. Объект не может наследоваться от двух других объектов.)
--------------------------------------------------------------

# React & Redux
1. **What is Virtual DOM?**
- Виртуальная `DOM` является представлением реальной `DOM` в памяти. `React` создает кэш структуры данных в памяти, вычисляет результирующие различия и затем эффективно обновляет отображаемую `DOM` браузера. Это позволяет программисту писать код, как будто вся страница отображается при каждом изменении, в то время как библиотеки React отображают только те подкомпоненты, которые действительно изменяются.

- The `Virtual DOM (VDOM)` is an in-memory representation of Real DOM. The representation of a UI is kept in memory and synced(синхронизируется) with the "real" DOM. It's a step that happens between the render function being called and the displaying of elements on the screen. This entire process is called `reconciliation`.  
--------------------------------------------------------------

2. **!!!Что такое JSX?**
  - `JSX` это технология, которая была представлена React.
  - `JSX` just provides syntactic sugar for the React.createElement(component, props, ...children) function.
  - Это смахивает на странный микс `JavaScript` и `HTML`, но в реальности это всё чистый `JavaScript` (именно поэтому слова `class` и `for` зарезервированные слова и вместо них используем `className` и `htmlFor`). 
  - `JSX` должен иметь обертку - Потому, что функция render() может отдать только один узел, так что в случае, когда вам надо вернуть двух потомков, просто добавьте родителя.
  - `JSX` транспилируется в:
    `ReactDOM.render(`
      `React.createElement('div', { id: 'test' },`
        `React.createElement('h1', null, 'A title'),`
        `React.createElement('p', null, 'A paragraph')`
      `),`
      `document.getElementById('myapp')`
    `)`
  - `JSX` позволяет компонентам полностью инкапсулировать их стили (через аттрибут `style`).
  - `JSX` предотвращает атаки, тк `ReactDOM` экранирует все значения, включенные в `JSX` перед тем как отрендерить их, т.е. преобразует в строку, а не как `innetHTML` => вредоносный скрипт не отработаeт.
  - `JSX` is a XML-like syntax extension to `ECMAScript` (the acronym stands for `JavaScript XML`). Basically it just provides syntactic sugar for the `React.createElement()` function, giving us expressiveness of JavaScript along with `HTML` like template syntax.
--------------------------------------------------------------

3. Рассказать про рендеринг коллекций и ключей. (Зачем нужен уникальный ключ, реконсилейшн алгоритм - процесс поиска изменений).

4. Как ты понимаешь, что перед тобой отдельный компонент? 
--------------------------------------------------------------

# Typescript
1. Множественное наследование в ТypeScript? (от классов, или implements interfaces)
(
  - классы - да, через миксины
  - An interface can extend multiple interfaces
)
--------------------------------------------------------------

# Angular
1. Провести сравнительную характеристику React и Angular.
(https://programmingwithmosh.com/react/react-vs-angular/)

--------------------------------------------------------------

2.Что такое директива (directive) в Angular? Назовите несколько основных директив.
(
  - Директива - атрибут или элемент, который дополняет существующий элемент DOM или представляет собой многократно используемый компонент DOM - виджет.
  - Директивы описывают изменение поведения или преобразование DOM модели, связанное с пользовательским атрибутом, именем элемента, или css классом. Директивы позволяют расширить HTML-синтаксис в декларативной форме.
  - Angular поставляется с набором директив, полезных для создания веб-приложений, но может быть расширен так, чтобы превратить HTML в декларативный предметно-ориентированный язык (DSL).
  - Несколько основных директив: ngApp , ngController, ngRepeat, ngModel, ngBind.)
  --------------------------------------------------------------

3. Каков жизненный цикл у компонентов?

(
    После создания компонента или директивы через вызов конструктора, Angular вызывает методы жизненного цикла в следующей последовательности в строго определенные моменты:

    ngOnChanges() - вызывается когда Angular переприсваивает привязанные данные к input properties. Метод получает объект SimpleChanges, со старыми и новыми значениями. Вызывается перед NgOnInit и каждый раз, когда изменяется одно или несколько связанных свойств.
    ngOnInit() - инициализирует директиву/компонент после того, как Angular впервые отобразит связанные свойства и устанавливает входящие параметры.
    ngDoCheck() - при обнаружении изменений, которые Angular не может самостоятельно обнаружить, реагирует на них.
    ngAfterContentInit() - вызывается после того, как Angular спроецирует внешний контент в отображение компонента или отображение с директивой. Вызывается единожды, после первого ngDoCheck().
    ngAfterContentChecked() - реагирует на проверку Angular-ом проецируемого содержимого. Вызывается после ngAfterContentInit() и каждый последующий ngDoCheck().
    ngAfterViewInit() - вызывается после инициализации отображения компонента и дочерних/директив. Вызывается единожды, после первого ngAfterContentChecked().
    ngAfterViewChecked() - реагирует на проверку отображения компонента и дочерних/директив. Вызывается после ngAfterViewInit() и каждый последующий ngAfterContentChecked().
    ngOnDestroy() - после уничтожения директивы/компонента выполняется очистка. Отписывает Observables и отключает обработчики событий, чтобы избежать утечек памяти.
)
  --------------------------------------------------------------
