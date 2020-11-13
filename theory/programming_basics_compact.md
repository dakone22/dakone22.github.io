
# 1. Синтаксис и семантика языков программирования. Алфавит языка Delphi Pascal. Описание синтаксиса языка: синтаксические диаграммы. Примеры.

**Синтаксис** -- правила, определяющие допустимые конструкции языка, построенные из символов его алфавита.

**Семантика** -- правила, определяющие смысл синтаксически корректных предложений. 

Алфавит языка программирования *Delphi Pascal* включает:
1. латинские буквы **без различия** строчных и прописных + символ `_` (считается как буква);
2. арабские цифры;
3. шестнадцатеричные цифры: `0..9`, `а..f` или `A..F`;
4. специальные символы: `+` `-` `*` `/` `=` `:=` `;` и т. д.;
5. служебные слова.

**Синтаксическая диаграмма** -- это направленный граф с одним входным ребром и одним выходным ребром и помеченными вершинами.

# 2. Представление данных в Delphi Pascal: константы и переменные. Классификация скалярных типов данных, операции над ними. Примеры. 

* Данные.
  1. **Константы** -- данные, не изменяемые в процессе выполнения программы.
      1. **Литералы** -- константы, указанные непосредственно в тексте программы.
      2. **Поименованные константы** -- константы, обращение к которым выполняется по имени. 
  2. **Переменные** -- поименованные данные, которые могут изменяться в процессе выполнения программы.

## Классификация типов данных языка

1. Простой
        1. Порядковые 
            1. Целые;
            2. Логические;
            3. Символ;
            4. *Перечисление;*
            5. *Отрезок (Интервал);*
        3. Вещественный
            1. Вещественные;
            2. Большое целое;

# 3. Совместимость типов данных и операции преобразования типов. Примеры. 

По правилам **совместимы**:
1. все целые типы между собой;
2. все вещественные типы между собой;
3. отрезок базового типа и базовый тип;
4. два отрезка одного и того же базового типа;
5. символ и строка.

### Неявное преобразование типов

Если типы результата и переменной не совпадают, но совместимы, то при выполнении присваивания выполняется **неявное автоматическое преобразование**.

### Явное преобразование типов

Для несовместимых типов результата и переменной, в которую его необходимо занести, при выполнении присваивания необходимо **явное преобразование типов**, например, посредством специальных функций:
* `trunc(x: float): int` или `int(x: float): int` -- преобразует вещественное число в целое, отбрасывая дробную часть.
* `round(x: float): int` -- округляет вещественное число до целого по правилам арифметики.
* `ord(c: ordinal): int` -- преобразует значение в его номер.
* `chr(x: int): Char` -- преобразует номер символа в символ.

# 4. Присваивание, условный оператор, оператор выбора. Синтаксис операторов, их особенности и примеры использования. 

## Присваивание `:=`

Используется для изменения значений переменных.
Формат: `<идентификатор_переменной> := <выражение>;`

Корректное выполнение оператора предполагает, что результат вычисления и переменная правой части **одного типа** или **совместимы по типу**.

## Условный оператор `if`

Оператор условной передачи управления используется при обработке вариантов вычислений и реализует конструкцию ветвления.

Формат: `if <логическое_выражение> then <оператор> [else <оператор>];`

*Оператором* может быть как простой оператор, так и составной оператор (блок операторов в операторных скобках `begin...end`)

## Оператор выбора `case`

Оператор позволяет программировать несколько вариантов решения.

Пример:
```pascal
case 1 + 2 * j of
    3:         z:=sin(x);
    -1..1, 10: z:=cos(x);
    else       z:=0;
end;
```

# 5. Операторы циклов Delphi Pascal. Синтаксис операторов, их особенности и примеры использования. 

### Операторы организации циклов

  * **Cчетный цикл** -- цикл, количество повторений которого известно или можно посчитать. Выход из такого цикла программируется по счетчику (`for-loop`).
  * **Итерационный цикл** -- цикл, количество повторений которого неизвестно или считается неизвестным при построении цикла. Выход из цикла программируется по выполнению или нарушению условия (`while-do`, `repeat-until`).
  * **Поисковый цикл** имеет два выхода: *нашли* и *перебрали все и не нашли*.

## Счётный цикл `for-loop`

Выполняется конкретное количество раз.
Формат: 
`for <переменная-счётчик> := <значение_от> to <значение_по> do <оператор>;` (если *от* < *по*)
`for <переменная-счётчик> := <значение_от> downto <значение_по> do <оператор>;` (если *от* > *по*)

Пример: 
```pascal
var i: Integer;
{...}
for i := 1 to 10 do
    begin
        x := x + 1;
        e := e / 10;
    end;
```

## Итерационные циклы

### `while-do`

Выполняется, пока *условие **истинно***.

Пример: 
```pascal
while abs(e) >= 1e-5 do
    begin
        x := x + 1;
        e := e / 10;
    end;
```

### `repeat-until`

Выполняется, до тех пор, пока *условие не станет **истинно*** (то есть пока условие ложно).
Первый раз один проход цикла выполняется в любом случае. 

Пример: 
```pascal
repeat
    x := x + 1;
    e := e / 10;
until abs(e) < 1e-5;
```

# 6. Поисковый цикл. Неструктурная и структурная реализации поискового цикла. 

**Поисковый цикл** -- особый вид цикла, который имеет два случая выхода:
1. нашли,
2. перебрали все элементы, но не нашли.

## Неструктурная реализация поискового цикла

```pascal
var
    found: boolean;

{...}
found := false;
while true do
    begin
        {операторы, выполняемые до проверки}
        
        if {проверка на то, нашли ли необходимое} then begin
                found := true;  // ставим флаг, что нашли
                break;          // прерываем цикл
            end;
        if {проверка на то, не перебрали ли всё} then
            break;
        
        {операторы, выполняемые после проверки}
    end;

if found then
    {нашли}
else
    {не нашли}
```

## Структурная реализация поискового цикла №1 (через `while-do`)

```pascal
var
    found: boolean;

{...}
{операторы, выполняемые до проверки}
found := {нашли ли необходимое};
while not (found) and not ({не перебрали ли всё}) do
    begin
        {операторы, выполняемые после проверки}
        {операторы, выполняемые до проверки}
        if {нашли ли необходимое} then
                found := true;  // ставим флаг, что нашли
    end;

if found then
    {нашли}
else
    {не нашли}
```

### Структурная реализация поискового цикла №2 (через `repeat-until`)

Примерный общий вид структурной реализации поискового цикла:
```pascal
var
    found: boolean;
{...}

found := false;
repeat
    {операторы, выполняемые после проверки}
    {операторы, выполняемые до проверки} // !!! 
                                         // тут отличается от первой структурной реализации:
                  // выполнится в первый раз в любой случае, в отличие от первой реализации!
    if {нашли ли необходимое} then
        found := true;                   // ставим флаг, что нашли
until (found) or ({всё перебрали});

if found then
    {нашли}
else
    {не нашли}
```

# 7. Массивы Delphi Pascal. Описание, операции над массивами и их элементами. Примеры. 

**Массив** -- это *упорядоченная* совокупность *однотипных* данных. Каждому элементу массива соответствует один или несколько *индексов порядкового типа*, определяющих положение элемента в массиве.

Формат: `array [<типы индекса>] of <тип элемента>` (*типы индекса перечисляются через запятую, если их больше одного*).

Количество типов индексов задает **размерность** массива.
**Тип индекса** -- порядковый -- определяет доступ к элементу.
**Тип элемента** -- любой кроме файла, в том числе массивы, строки и т.п.
Массив в памяти не может занимать более 2 Гб (из-за технических ограничений).

### Операции над массивами

1. Операция присваивания (только для массивов одного типа)
2. Доступ к элементу массива (**прямой** и **косвенный доступ**)
3. Ввод/вывод массивов осуществляется поэлементно:

# 8. Строки Delphi Pascal. Описание, операции над строками и их элементами. Примеры. 

**Строка** -- последовательность символов (*фактически, массив символов*).

Формат (обычно): `string` или `string[<размер>]`, где *размер* -- максимальная длина строки.

### Операции над строками

1. Присваивание строк:
2. Обращение к элементу:
3. **Конкатенация** (сцепление) строк:
4. **Операции отношения** -- выполняется попарным сравнением кодов символов, результат определяется по отношению кодов первых различных символов:
5. Ввод-вывод  строк:

# 9. Множества Delphi Pascal. Описание, операции над множествами и их элементами. Примеры. 

**Множество** -- *неупорядоченная* совокупность *неповторяющихся* элементов.

Формат: `set of <базовый_тип>`.
Тип элементов -- *порядковый*, но количество элементов **не должно превышать 256**. (То есть нельзя использовать `Word`, `Integer`, `UInt64` и т. д., так как они явно больше 256)

### Операции над множествами

1. Присваивание.
2.  Объединение, пересечение и дополнение:
    * `A + B` ($A \cup B$) -- объединение множеств `А` и `B` -- множество, состоящее из элементов, принадлежащих множествам `А` и `B`.
    * `A * B` ($A \cap B$) -- пересечение множеств `А` и `B` -- множество, состоящее из элементов, принадлежащих одновременно и множеству `А` и множеству `B`.
    * `A - B` ($A \setminus B$) -- дополнение множества `А` до `B` -- множество, состоящее из тех элементов множества `А`, которые не принадлежат множеству `B`.
3.  Операции отношения:
    * `A = B` ($A = B$) -- проверка совпадения множеств А и B (если совпадают -- `true`).
    * `A <> B` ($A \not= B$) -- проверка не совпадения множеств А и B (не совпадают -- `true`).
    * `A <= B` ($A \subseteq B$) -- проверка нестрогого вхождения A в B (если входит -- `true`).
    * `A > B` ($A \supset B$) -- проверка строгого вхождения B в A (если входит -- `true`).
4. Проверка вхождения элемента во множество:
    `x in A` ($x \in A$) -- входит ли элемент `x` в множество `A` (если входит -- `true`).

# 10. Записи Delphi Pascal. Описание, операции над записями и их элементами. Примеры. 

**Запись** -- это структура данных, образованная *фиксированным числом разнотипных компонентов*, называемых **полями** записи

```pascal
type
    EntryType = (Book, Magazine);
    Entry = record
        autor, title: String;
        year : 1..2000;
        case tag: EntryType of
            Book: (publisher, city: String);
            Magazine: (
                magName: String; 
                volume, issue: Integer
            );            // case не имеет своего end'а и пишется последним.
    end;
```

### Операции над записями

1. Присваивание записей одного типа.
2. Доступ к полям записи (*точечная нотация*, *оператор доступа `with`*).
3. Ввод и вывод записей осуществляется по полям.

# 11. Процедуры и функции. Определение, описание, особенности. Примеры. 

**Процедуры и функции** -- самостоятельные фрагменты программы, соответствующим образом оформленные и вызываемые по имени (программные блоки).

Общий вид программного блока: `Заголовок блока -> Раздел описаний -> Раздел операторов`

### Процедура

Заголовок начинается с служебного слова `procedure`.
После работы процедура не возвращает значений.

### Функция

Заголовок начинается с служебного слова `function` и заканчивается возвращаемым типом. После работы функции, она возвращает значение типа, который указан в заголовке как возвращаемый.

Чтобы вернуть какое-то значение из функции, в процессе её выполнения необходимо присвоить системной переменной *`<идентификатор_функции>`* (или `result`, при включенном расширенном синтаксисе `{$X+}`) это необходимое значение.

# 12. Способы передачи данных в подпрограмму на Delphi Pascal. Примеры. 

Подпрограмма может получать данные из основной программы:
1. **неявно** -- с использованием свойства доступности глобальных переменных;
2. **явно** -- через параметры.

Очевидно, что *явная* передача значительно лучше, так как позволяет делать подпрограммы более универсальными и независимыми.

## Типы параметров

* **Параметры-значения** при описании подпрограммы не помечаются. По факту в эту переменную *копируется* значение переданного аргумента, поэтому изменение этой переменной в подпрограмме не отразится на внешней.

* **Параметры-переменные** при описании подпрограммы помечаются служебным словом `var`.
  По факту происходит передача переменной *по адресу*, то есть все изменения такой переменной в подпрограмме **отразятся на внешней**!

* **Параметры-константы** при описании подпрограммы помечаются служебным словом `const`.
  Как и с *параметрами-переменными*, по факту происходит передача переменной *по адресу*, но при попытке изменить значение переменной в подпрограмме, вызывается ошибка. То есть изменять значение в подпрограмме запрещено. 

# 13. Локальные и глобальные переменные, законы «видимости» идентификаторов. Примеры. 

|Классы переменных|Время жизни|Доступность|
|--|--|--|
|**Глобальные** -- объявленные в основной программе|От запуска до завершения программы|Из любого места программы, включая подпрограммы\*|
|**Локальные** -- объявленные в подпрограмме|От вызова подпрограммы до возврата управления|Из подпрограммы и подпрограмм, вызываемых из нее\*|
**\*** -- при отсутствии перекрытия имен

# 14. Формальные и фактические параметры подпрограмм Delphi Pascal. Примеры. 

Параметры, описанные в заголовке -- **формальные**.

При вызове подпрограммы необходимо определить **фактические** значения этих параметров -- аргументы (константы и переменные).

> Вот только кто вообще их так называет?
> Обычно их называют **параметрами** и **аргументами** соответственно.

*Формальные* и *фактические* параметры должны соответствовать по количеству, типу и порядку:

# 15. Параметры-строки, параметры-массивы. Примеры. 

Структурные типы параметров должны быть **предварительно объявлены**.
```pascal
type
    IntArr = array[1..100] of Integer;
    MyStr = string[25];

function sum(arr: IntArr; n: Integer): integer;
{...}

procedure test_string(str: MyStr);
{...}

var
    my_arr: IntArr;
    my_str: MyStr;
    {...}

begin
    {...}
    writeLn('Sum(arr) = ', sum(my_arr, n));
    test_string(my_str);
end.
```

# 16. Принципы разработки универсальных подпрограмм: «открытые» массивы и строки. Примеры. 

# Открытые массивы

**Открытый массив** -- конструкция описания типа массива без указания типа индексов. 
Используется только при объявлении *формальных параметров*.

```pascal
array of Single;
array of Integer;
```

С помощью открытых массивов можно делать более *универсальные* подпрограммы.

**Индексы открытого массива всегда начинаются с `0`-го.**

Размер можно:
* передать через дополнительный параметр;
* получить, используя функцию `high(<идентификатор_массива>)`.


## ~~Открытые строки~~

~~**Для строк, передаваемых в подпрограмму как параметр-переменная, осуществляет контроль длины строки.**~~

~~Чтобы избежать его необходимо использовать «*открытые*» строки (`openstring`).~~

> Устаревшая информация. В новых версиях проблем с передачей строк быть не должно.

# 17. Принципы разработки универсальных подпрограмм: нетипизированные параметры, параметры процедурного типа. Примеры. 

## Нетипизированные параметры.

**Нетипизированные параметры** -- *параметры-переменные*, тип которых при объявлении не указан.

Для приведения нетипизированного параметра к определенному типу можно использовать:
1. автоопределенное преобразование типов:
   ```pascal
   procedure proc(var a);
   {...}
   b := Integer(a) + 10;
   ```

2. наложенное описание переменной определенного типа:
   ```pascal
   type
       TType = (TReal, TInteger);
   
   procedure proc(var a; t: TType);
   var
       r: Real absolute a;
       i: Integer absolute a;
   
   {...}
       if t = TReal then
           {используем переменную `r`}
       else
           {используем переменную `i`}
   ```
   По факту, тут `a` является ссылкой на какой-то адрес в памяти, но нужный размер в памяти нам неизвестен. С помощью наложения мы делаем несколько видов переменных, *накладывая* на адрес переменной `a` разные типы.


## Параметры процедурного типа

Параметры процедурного типа используются для передачи в подпрограмму имен процедур и функций.

Для объявления процедурного типа используется заголовок подпрограммы, в котором отсутствует имя:
```pascal
type
    Proc = procedure (a, b, c: Real; var d: Real);
    UnaryFunc = function(x: Double): Double;
```

Значениями переменных процедурных типов являются идентификаторы процедур и функций с соответствующими заголовками.

# 18. Структура модуля Delphi Pascal. Законы видимости идентификаторов. Доступ к «перекрытым» идентификаторам. Примеры. 

**Модуль** -- это автономно компилируемая коллекция программных ресурсов, предназначенных для использования другими модулями и программами

## Структура модуля:
```pascal
unit <имя_модуля>;  // Имя модуля должно совпадать с 
                    // именем файла, в котором он описан.

interface
    <интерфейсная_секция>

implementation
    <секция_реализации>

[initialization
    <секция_инициализации>

[finalization
    <секция_завершения>]]
end.
```

## Законы видимости идентификаторов. Доступ к «перекрытым» идентификаторам

**Ресурсы модуля перекрываются ресурсами программы и ранее указанных модулей.**

Для доступа к перекрытым ресурсам модуля используют точечную нотацию: `<имя_модуля>.<имя_ресурса>`

Пример:
![identificators_intersection](https://i.imgur.com/R0qXc5n.png)


# 19. Рекурсия. Виды рекурсии. Особенности программирования. Достоинства и недостатки. Пример. 


**Рекурсия** -- организация вычислений, при которой процедура или функция обращаются к самим себе.

Различают *явную* и *косвенную* рекурсии. 
При *явной* -- в теле подпрограммы существует вызов самой себя, при *косвенной* -- вызов осуществляется в подпрограммах, вызываемых из рассматриваемой.

Косвенная рекурсия требует предопределения `forward`.

# 20. Адресация динамической памяти: понятие адреса, операции получения адреса и разыменования. Процедуры получения памяти и освобождения ее. Примеры. 

Минимальная адресуемая единица памяти -- **байт**.

**Физический адрес** $А_ф$ -- номер байта оперативной памяти.

Адресация по схеме «база+смещение»: $А_ф = А_б + А_{см}$,
где $А_б$ -- адрес базы -- адрес, относительно которого считают остальные адреса;
$А_{см}$ -- смещение -- расстояние от базового адреса до физического.

**Указатель** -- тип данных, используемый для хранения **смещений**.
В памяти занимает 4 байта, адресует сегмент размером $V = 2^{32} = 4$ ГБ.
Базовый адрес = адрес сегмента.

Различают указатели:
* *типизированные* -- адресующие данные конкретного типа;
* *нетипизированные* -- не связанные с данными определенного типа.

### Операции с указателями

1. **Получение адреса**: оператор `@`. Результат операции -- указатель типа `pointer` -- может присвоен любому указателю.
2. **Доступ к данным** по указателю (**операция разыменования**). Полученное значение имеет тип, совпадающий с базовым типом данных указателя. *Нетипизированные указатели разыменовывать нельзя*.

### Процедуры для работы с памятью

1. Процедура `new(var p: ^<тип>)` -- выделяет память для размещения переменной, размер определяется типом указателя.
2. Процедура `dispose(var p: ^<тип>)` -- освобождает выделенную память.
3. Процедура `getMem(var p: Pointer; size: Integer)` -- выделяет указанное количество памяти и помещает ее адрес в указатель.
4. Процедура `freeMem(var p: Pointer[; size: Integer])` -- освобождает выделенную память.
5. Процедура `sizeOf(x): Integer` -- возвращает размер объекта в байтах.
   ```pascal
   type
       ByteArr = array[1..100] of Byte;
   
   var
       buffer: ^ByteArr;
   
   {...}
   getMem(buffer, sizeOf(ByteArr));
   buffer^[1] := 125;
   {...}
   freeMem(buffer, sizeOf(Byte) * 100); 
   ```

# 21. Списковые структуры данных. Классификация и основные приемы работы с ними: создание элемента, добавление элемента к списку, удаление элемента из списка. Область применения списковых структур данных. Пример. 

**Список** -- способ организации данных, предполагающий использование указателей для определения следующего элемента.

Элемент списка состоит из двух частей: *информационной* и *адресной*.

*Информационная* часть содержит поля данных.
*Адресная* -- включает от одного до n указателей, содержащих адреса следующих элементов. Количество связей, между соседними элементами списка определяет его связность: односвязные, двусвязные, n-связные.

### Виды списков

* **Линейный односвязный** -- у каждого элемента есть указатель на следующий после него элемент (кроме, соответственно, последнего).
* **Линейный двусвязный** -- у каждого элемента есть указатель на следующий и предыдущий элементы (кроме крайних, у них нет одного соответственного).
* **Кольцевой односвязный** -- у каждого элемента есть указатель на следующий после него элемент, а у последнего есть указатель на первый.
* **Кольцевой двусвязный** -- у каждого элемента есть указатель на следующий и предыдущий элементы, а у первого и последнего есть указатели на последний и первый соответственно.
* **Сетевой *n*-связный** -- у каждого есть сразу несколько указателей на другие элементы.

# 22. Основы файловой системы: файл, каталог, дисковод, полное имя файла, внутреннее представление информации в файле. Файловая переменная. Операции открытия и закрытия файлов. Примеры. 

**Файл** -- поименованная последовательность элементов данных (компонентов файла), хранящихся, как правило, во внешней памяти.
Как исключение данные файла могут не храниться, а вводиться с *внешних устройств* (*ВУ*), например клавиатуры или выводиться на *ВУ*.
Полное имя файла включает:
`<Имя диска>:<Список имен каталогов>\<Имя файла>.<Расширение>`

**Файл языка Pascal** -- последовательность однотипных компонентов: файл записей, файл целых чисел, файл строк.

В зависимости от типа компонентов различают три типа файлов: **типизированные**, **текстовые** и **нетипизированные**.

*Количество компонентов* файла при объявлении файловой переменной не указывается.
*Максимальный размер* файла определяется свободным пространством на устройстве, например, диске.
Физически операции ввода-вывода с файлами выполняются *с использованием буфера*.

Доступ к компонентам файла осуществляется через **указатель файла**.
При выполнении операции чтения или записи указатель **автоматически** перемещается на следующий компонент.
После вывода последнего компонента файла система пишет специальную запись -- **маркер «*Конец файла*»** (байт `#26`).
При обнаружении во время операции чтения маркера конца файла -- операция завершается. Попытка читать маркер вызывает прерывание по ошибке чтения.

Процедура `assign` или `assignFile (var f; path: String)` (*предпочтительнее*) -- связывает файловую переменную `f` с файлом, имя которого указано в строке `path`.

#### Инициализация файловой переменной

Процедура `assign` или `assignFile (var f; path: String)` (*предпочтительнее*) -- связывает файловую переменную `f` с файлом, имя которого указано в строке `path`.

Если файл находится в текущем каталоге, то достаточно задать имя файла и его расширение. В противном случае необходимо указать полное имя файла.

#### Открытие файла

При открытии файла необходимо задать направление передачи данных: запись или чтение. Кроме того текстовый файл можно открыть для добавления компонентов.

1. Процедура `reSet(var f)` -- открывает файл для чтения данных.
   Устанавливает указатель файла на первый компонент. Если файл не существует, выдается сообщение об ошибке.

2. Процедура `reWrite(var f)` -- открывает файл для записи.
   Если указанный файл существовал, то он уничтожается без выдачи предупреждения пользователю, иначе он создается и указатель устанавливается на начало.

3. Процедура `append(var f: Text)` -- открывает текстовый файл для добавления данных.
   Указатель файла устанавливается на конец файла.

#### Закрытие файла

Процедура `close` или `closeFile(var f)` - выполняет закрытие файла. При этом вновь созданный файл регистрируется в каталоге.

Процедура закрытия файла обеспечивает **вывод оставшихся компонентов из буфера в файл**.

Связь файловой переменной с файлом при закрытии сохраняется, поэтому при продолжении обработки повторно процедуру `assignFile()` можно не выполнять.

# 23. Текстовые файлы. Внутреннее представление информации в файле. Операции над файлами. Пример. 


**Текстовый файл** -- файл, компонентами которого являются символьные строки переменной длины, заканчивающиеся специальным маркером -- **маркером «Конец строки»**.

Текстовые файлы используют для хранения и обработки символов, строк, символьных массивов. Числовые и логические данные при записи в текстовые файлы должны преобразовываться в символьные строки.

Текстовый файл можно открыть для записи, чтения и добавления записей в конец. Файл, открытый для записи, не может использоваться для чтения и наоборот.

## Операции с текстовыми файлами

1. Функция `EOLn([var f]): Boolean` -- возвращает `TRUE`, если во входном текстовом файле достигнут маркер конца строки; при отсутствии файловой переменной проверяется файл `INPUT`, связанный с клавиатурой.
   * При работе с *клавиатурой* функция `EOLn` возвращает `TRUE`, если **последним** считанным был символ `#13`.
   * При работе с *диском* функция `EOLn` возвращает `TRUE`, если **следующим** считанным будет символ `#13`.
2. Процедура `read([var f: text;] v1, v2, {...} vn)`
3. Процедура `readLn([var f: text;] v1, v2, {...} vn)` 
4. Процедура `write([var f: text;] v1, v2, {...} vn)` 
5. Процедура `writeLn([var f: text;] v1, v2, {...} vn)`
7. Процедура `seekEOLn([var f]): Boolean` -- пропускает пробелы и знаки табуляции до маркера конца строки или до первого значащего символа и возвращает `TRUE`, при обнаружении маркера.
8. Процедура `SeekEOF([var f]): Boolean` -- пропускает все пробелы, знаки табуляции и маркеры конца строки до маркера конца файла или до первого значащего символа и возвращает `TRUE` при обнаружении маркера.

# 24. Типизированные файлы: внутреннее представление информации в файле. Операции над файлами. Пример. 

**Типизированный файл** -- файл, все компоненты которого одного типа, заданного при объявлении файловой переменной.

Компоненты хранятся на диске во *внутреннем* (двоичном) формате.

Типизированный файл можно открыть для записи и чтения. Файл, открытый для записи, может использоваться для чтения. В файл, открытый для чтения, можно писать.

Поскольку размер компонентов **одинаков**, принципиально возможен не только последовательный, но и **прямой доступ**.

## Процедуры и функции обработки типизированных файлов

1. Процедура `read(var f; c1, c2, {...} cn)`
2. Процедура `write(var f; c1, c2, {...} cn)`
3. Процедура `seek(var f; numcomp: LongInt)`
4. Функция `fileSize(var f): LongInt`
5. Функция `filePos(var f): LongInt`
6. Процедура `truncate(var f)` -- выполняет «*усечение*» файла.


# 25. Нетипизированные файлы. Внутреннее представление информации в файле. Операции над файлами. Пример. 

**Нетипизированными** называют файлы, объявленные без указания типа компонентов.

Операции чтения и записи с такими файлами осуществляются блоками, что позволяет организовать высокоскоростной обмен данными между диском и памятью. Отсутствие типа делает эти файлы совместимыми с любыми другими.

Нетипизированные файлы, как и типизированные, допускают организацию прямого доступа.
Нетипизированный файл можно открыть для записи и для чтения:
```pascal
reSet(var f[; recsize: Word]);
```
```pascal
reWrite(var f[; recsize: Word]);
```
где `recsize` -- размер записи файла в байтах. Длину записи задают кратной 512 байт, например: 1024, 2048. Если длина записи не указана, она принимается равной 128.

## Процедуры и функции обработки нетипизированных файлов

1. Процедура `blockRead(var f: file; var buf; count: Word[; var res: Word])` -- осуществляет чтение блока записей из файла в буфер `buf`.
   Параметр `res` будет содержать количество фактически обработанных записей. Если последняя запись -- неполная, то значение параметра `res` ее не учтет.

2. Процедура `blockWrite(var f: file; var buf; count: Word[; var res: Word])` -- осуществляет запись блока из буфера `buf` в файл.

# 26. Классы консольного режима Delphi: описание классов, поля и методы, объявление объектов класса, доступ к полям и методам объекта, ограничение доступа. Пример. 

**Класс** -- это структурный тип данных, который включает описание полей данных, а также процедур и функций, работающих с этими полями данных.
C точки зрения синтаксиса **класс** -- структурный тип данных, в котором помимо полей разрешается описывать *прототипы* (заголовки) процедур и функций, работающих с этими полями данных.

Применительно к классам такие процедуры и функции получили название **методов**.
**Объект-переменная** -- переменная типа «класс».

```pascal
var a: TRoom = (length: 3.5; width: 5.1);
```

|Модификатор доступа|Доступность|
|--|--|
|`public`|поля и методы, доступны из других модулей|
|`private`|поля и методы, доступны только в пределах модуля|
|`protected`|поля и методы, доступны только в классах потомках|
|`published`|поля и методы, видимы в инспекторе объектов|

По умолчанию для всех полей используется модификатор `public`.

# 27. Классы консольного режима Delphi: Способы инициализация полей. Неявный параметр Self. Пример. 

Любой метод неявно получает параметр **`self`** -- ссылку (адрес) на поля объекта, и обращение к полям происходит через это имя.

```pascal
function TRoom.square;
begin
    result := self.length * self.width;
End;
```
При необходимости эту ссылку можно указывать явно:

`@self` -- адрес области полей данных объекта.


# 28. Процедурная и объектная декомпозиция. Диаграммы классов. Отношения между классами. Примеры. 

**Процедурная декомпозиция** -- процесс разбиения программы на подпрограммы.

**Структурной** называют декомпозицию, если:
* каждая подпрограмма имеет один вход и один выход;
* подпрограммы нижних уровней не вызывают подпрограмм верхних уровней;
* размер подпрограммы не превышает 40-50 операторов;
* в алгоритме использованы только структурные конструкции.

**Объектная декомпозиция** -- процесс представления предметной области задачи в виде отдельных функциональных элементов (объектов предметной области), обменивающихся в процессе выполнения программы входными воздействиями (сообщениями) .

1. **Наследование** -- механизм, позволяющий строить класс на базе более простого посредством добавления полей и определения новых методов.

   При этом исходный класс, на базе которого выполняется построение, называют *родительским* или *базовым*, а строящейся класс -- *потомком* или *производным* классом.

   Если при наследовании какие-либо методы переопределяются, то такое наследование называется полиморфным.
   
   ![](https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0JrQu9Cw0YHRgdCg0L7QtNC40YLQtdC70YwgPHwtLSDQmtC70LDRgdGB0J_QvtGC0L7QvNC-0LoiLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCIsInRoZW1lVmFyaWFibGVzIjp7ImJhY2tncm91bmQiOiJ3aGl0ZSIsInByaW1hcnlDb2xvciI6IiNFQ0VDRkYiLCJzZWNvbmRhcnlDb2xvciI6IiNmZmZmZGUiLCJ0ZXJ0aWFyeUNvbG9yIjoiaHNsKDgwLCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5Qm9yZGVyQ29sb3IiOiJoc2woMjQwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInNlY29uZGFyeUJvcmRlckNvbG9yIjoiaHNsKDYwLCA2MCUsIDgzLjUyOTQxMTc2NDclKSIsInRlcnRpYXJ5Qm9yZGVyQ29sb3IiOiJoc2woODAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeVRleHRDb2xvciI6IiMxMzEzMDAiLCJzZWNvbmRhcnlUZXh0Q29sb3IiOiIjMDAwMDIxIiwidGVydGlhcnlUZXh0Q29sb3IiOiJyZ2IoOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSkiLCJsaW5lQ29sb3IiOiIjMzMzMzMzIiwidGV4dENvbG9yIjoiIzMzMyIsIm1haW5Ca2ciOiIjRUNFQ0ZGIiwic2Vjb25kQmtnIjoiI2ZmZmZkZSIsImJvcmRlcjEiOiIjOTM3MERCIiwiYm9yZGVyMiI6IiNhYWFhMzMiLCJhcnJvd2hlYWRDb2xvciI6IiMzMzMzMzMiLCJmb250RmFtaWx5IjoiXCJ0cmVidWNoZXQgbXNcIiwgdmVyZGFuYSwgYXJpYWwiLCJmb250U2l6ZSI6IjE2cHgiLCJsYWJlbEJhY2tncm91bmQiOiIjZThlOGU4Iiwibm9kZUJrZyI6IiNFQ0VDRkYiLCJub2RlQm9yZGVyIjoiIzkzNzBEQiIsImNsdXN0ZXJCa2ciOiIjZmZmZmRlIiwiY2x1c3RlckJvcmRlciI6IiNhYWFhMzMiLCJkZWZhdWx0TGlua0NvbG9yIjoiIzMzMzMzMyIsInRpdGxlQ29sb3IiOiIjMzMzIiwiZWRnZUxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJhY3RvckJvcmRlciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImFjdG9yQmtnIjoiI0VDRUNGRiIsImFjdG9yVGV4dENvbG9yIjoiYmxhY2siLCJhY3RvckxpbmVDb2xvciI6ImdyZXkiLCJzaWduYWxDb2xvciI6IiMzMzMiLCJzaWduYWxUZXh0Q29sb3IiOiIjMzMzIiwibGFiZWxCb3hCa2dDb2xvciI6IiNFQ0VDRkYiLCJsYWJlbEJveEJvcmRlckNvbG9yIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwibGFiZWxUZXh0Q29sb3IiOiJibGFjayIsImxvb3BUZXh0Q29sb3IiOiJibGFjayIsIm5vdGVCb3JkZXJDb2xvciI6IiNhYWFhMzMiLCJub3RlQmtnQ29sb3IiOiIjZmZmNWFkIiwibm90ZVRleHRDb2xvciI6ImJsYWNrIiwiYWN0aXZhdGlvbkJvcmRlckNvbG9yIjoiIzY2NiIsImFjdGl2YXRpb25Ca2dDb2xvciI6IiNmNGY0ZjQiLCJzZXF1ZW5jZU51bWJlckNvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IiOiJyZ2JhKDEwMiwgMTAyLCAyNTUsIDAuNDkpIiwiYWx0U2VjdGlvbkJrZ0NvbG9yIjoid2hpdGUiLCJzZWN0aW9uQmtnQ29sb3IyIjoiI2ZmZjQwMCIsInRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJ0YXNrQmtnQ29sb3IiOiIjOGE5MGRkIiwidGFza1RleHRMaWdodENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dENvbG9yIjoid2hpdGUiLCJ0YXNrVGV4dERhcmtDb2xvciI6ImJsYWNrIiwidGFza1RleHRPdXRzaWRlQ29sb3IiOiJibGFjayIsInRhc2tUZXh0Q2xpY2thYmxlQ29sb3IiOiIjMDAzMTYzIiwiYWN0aXZlVGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsImFjdGl2ZVRhc2tCa2dDb2xvciI6IiNiZmM3ZmYiLCJncmlkQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JrZ0NvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCb3JkZXJDb2xvciI6ImdyZXkiLCJjcml0Qm9yZGVyQ29sb3IiOiIjZmY4ODg4IiwiY3JpdEJrZ0NvbG9yIjoicmVkIiwidG9kYXlMaW5lQ29sb3IiOiJyZWQiLCJsYWJlbENvbG9yIjoiYmxhY2siLCJlcnJvckJrZ0NvbG9yIjoiIzU1MjIyMiIsImVycm9yVGV4dENvbG9yIjoiIzU1MjIyMiIsImNsYXNzVGV4dCI6IiMxMzEzMDAiLCJmaWxsVHlwZTAiOiIjRUNFQ0ZGIiwiZmlsbFR5cGUxIjoiI2ZmZmZkZSIsImZpbGxUeXBlMiI6ImhzbCgzMDQsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlMyI6ImhzbCgxMjQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNCI6ImhzbCgxNzYsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNSI6ImhzbCgtNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU2IjoiaHNsKDgsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsImZpbGxUeXBlNyI6ImhzbCgxODgsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSJ9fSwidXBkYXRlRWRpdG9yIjpmYWxzZX0)

2. **Композиция** -- механизм, позволяющий включать несколько объектов других классов в конструируемый.
      ![](https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0J7RgdC90L7QstC90L7QudCa0LvQsNGB0YEgXCIxXCIgKi0tIFwiMVwiINCa0LvQsNGB0YHQp9Cw0YHRgtGMIiwibWVybWFpZCI6eyJ0aGVtZSI6ImRlZmF1bHQiLCJ0aGVtZVZhcmlhYmxlcyI6eyJiYWNrZ3JvdW5kIjoid2hpdGUiLCJwcmltYXJ5Q29sb3IiOiIjRUNFQ0ZGIiwic2Vjb25kYXJ5Q29sb3IiOiIjZmZmZmRlIiwidGVydGlhcnlDb2xvciI6ImhzbCg4MCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwicHJpbWFyeUJvcmRlckNvbG9yIjoiaHNsKDI0MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJzZWNvbmRhcnlCb3JkZXJDb2xvciI6ImhzbCg2MCwgNjAlLCA4My41Mjk0MTE3NjQ3JSkiLCJ0ZXJ0aWFyeUJvcmRlckNvbG9yIjoiaHNsKDgwLCA2MCUsIDg2LjI3NDUwOTgwMzklKSIsInByaW1hcnlUZXh0Q29sb3IiOiIjMTMxMzAwIiwic2Vjb25kYXJ5VGV4dENvbG9yIjoiIzAwMDAyMSIsInRlcnRpYXJ5VGV4dENvbG9yIjoicmdiKDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxLCA5LjUwMDAwMDAwMDEpIiwibGluZUNvbG9yIjoiIzMzMzMzMyIsInRleHRDb2xvciI6IiMzMzMiLCJtYWluQmtnIjoiI0VDRUNGRiIsInNlY29uZEJrZyI6IiNmZmZmZGUiLCJib3JkZXIxIjoiIzkzNzBEQiIsImJvcmRlcjIiOiIjYWFhYTMzIiwiYXJyb3doZWFkQ29sb3IiOiIjMzMzMzMzIiwiZm9udEZhbWlseSI6IlwidHJlYnVjaGV0IG1zXCIsIHZlcmRhbmEsIGFyaWFsIiwiZm9udFNpemUiOiIzMnB4IiwibGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsIm5vZGVCa2ciOiIjRUNFQ0ZGIiwibm9kZUJvcmRlciI6IiM5MzcwREIiLCJjbHVzdGVyQmtnIjoiI2ZmZmZkZSIsImNsdXN0ZXJCb3JkZXIiOiIjYWFhYTMzIiwiZGVmYXVsdExpbmtDb2xvciI6IiMzMzMzMzMiLCJ0aXRsZUNvbG9yIjoiIzMzMyIsImVkZ2VMYWJlbEJhY2tncm91bmQiOiIjZThlOGU4IiwiYWN0b3JCb3JkZXIiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJhY3RvckJrZyI6IiNFQ0VDRkYiLCJhY3RvclRleHRDb2xvciI6ImJsYWNrIiwiYWN0b3JMaW5lQ29sb3IiOiJncmV5Iiwic2lnbmFsQ29sb3IiOiIjMzMzIiwic2lnbmFsVGV4dENvbG9yIjoiIzMzMyIsImxhYmVsQm94QmtnQ29sb3IiOiIjRUNFQ0ZGIiwibGFiZWxCb3hCb3JkZXJDb2xvciI6ImhzbCgyNTkuNjI2MTY4MjI0MywgNTkuNzc2NTM2MzEyOCUsIDg3LjkwMTk2MDc4NDMlKSIsImxhYmVsVGV4dENvbG9yIjoiYmxhY2siLCJsb29wVGV4dENvbG9yIjoiYmxhY2siLCJub3RlQm9yZGVyQ29sb3IiOiIjYWFhYTMzIiwibm90ZUJrZ0NvbG9yIjoiI2ZmZjVhZCIsIm5vdGVUZXh0Q29sb3IiOiJibGFjayIsImFjdGl2YXRpb25Cb3JkZXJDb2xvciI6IiM2NjYiLCJhY3RpdmF0aW9uQmtnQ29sb3IiOiIjZjRmNGY0Iiwic2VxdWVuY2VOdW1iZXJDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yIjoicmdiYSgxMDIsIDEwMiwgMjU1LCAwLjQ5KSIsImFsdFNlY3Rpb25Ca2dDb2xvciI6IndoaXRlIiwic2VjdGlvbkJrZ0NvbG9yMiI6IiNmZmY0MDAiLCJ0YXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwidGFza0JrZ0NvbG9yIjoiIzhhOTBkZCIsInRhc2tUZXh0TGlnaHRDb2xvciI6IndoaXRlIiwidGFza1RleHRDb2xvciI6IndoaXRlIiwidGFza1RleHREYXJrQ29sb3IiOiJibGFjayIsInRhc2tUZXh0T3V0c2lkZUNvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dENsaWNrYWJsZUNvbG9yIjoiIzAwMzE2MyIsImFjdGl2ZVRhc2tCb3JkZXJDb2xvciI6IiM1MzRmYmMiLCJhY3RpdmVUYXNrQmtnQ29sb3IiOiIjYmZjN2ZmIiwiZ3JpZENvbG9yIjoibGlnaHRncmV5IiwiZG9uZVRhc2tCa2dDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQm9yZGVyQ29sb3IiOiJncmV5IiwiY3JpdEJvcmRlckNvbG9yIjoiI2ZmODg4OCIsImNyaXRCa2dDb2xvciI6InJlZCIsInRvZGF5TGluZUNvbG9yIjoicmVkIiwibGFiZWxDb2xvciI6ImJsYWNrIiwiZXJyb3JCa2dDb2xvciI6IiM1NTIyMjIiLCJlcnJvclRleHRDb2xvciI6IiM1NTIyMjIiLCJjbGFzc1RleHQiOiIjMTMxMzAwIiwiZmlsbFR5cGUwIjoiI0VDRUNGRiIsImZpbGxUeXBlMSI6IiNmZmZmZGUiLCJmaWxsVHlwZTIiOiJoc2woMzA0LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTMiOiJoc2woMTI0LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTQiOiJoc2woMTc2LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTUiOiJoc2woLTQsIDEwMCUsIDkzLjUyOTQxMTc2NDclKSIsImZpbGxUeXBlNiI6ImhzbCg4LCAxMDAlLCA5Ni4yNzQ1MDk4MDM5JSkiLCJmaWxsVHlwZTciOiJoc2woMTg4LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkifX0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)
   
3. **Наполнение** (***агрегация***) -- механизм, позволяющих включать указатели на объекты других классов в конструируемый.
      ![](https://mermaid.ink/svg/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAg0JrQu9Cw0YHRgdCQ0LPRgNC10LPQsNGCIG8tLSBcIjAuLipcIiDQmtC70LDRgdGB0KfQsNGB0YLRjCIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0IiwidGhlbWVWYXJpYWJsZXMiOnsiYmFja2dyb3VuZCI6IndoaXRlIiwicHJpbWFyeUNvbG9yIjoiI0VDRUNGRiIsInNlY29uZGFyeUNvbG9yIjoiI2ZmZmZkZSIsInRlcnRpYXJ5Q29sb3IiOiJoc2woODAsIDEwMCUsIDk2LjI3NDUwOTgwMzklKSIsInByaW1hcnlCb3JkZXJDb2xvciI6ImhzbCgyNDAsIDYwJSwgODYuMjc0NTA5ODAzOSUpIiwic2Vjb25kYXJ5Qm9yZGVyQ29sb3IiOiJoc2woNjAsIDYwJSwgODMuNTI5NDExNzY0NyUpIiwidGVydGlhcnlCb3JkZXJDb2xvciI6ImhzbCg4MCwgNjAlLCA4Ni4yNzQ1MDk4MDM5JSkiLCJwcmltYXJ5VGV4dENvbG9yIjoiIzEzMTMwMCIsInNlY29uZGFyeVRleHRDb2xvciI6IiMwMDAwMjEiLCJ0ZXJ0aWFyeVRleHRDb2xvciI6InJnYig5LjUwMDAwMDAwMDEsIDkuNTAwMDAwMDAwMSwgOS41MDAwMDAwMDAxKSIsImxpbmVDb2xvciI6IiMzMzMzMzMiLCJ0ZXh0Q29sb3IiOiIjMzMzIiwibWFpbkJrZyI6IiNFQ0VDRkYiLCJzZWNvbmRCa2ciOiIjZmZmZmRlIiwiYm9yZGVyMSI6IiM5MzcwREIiLCJib3JkZXIyIjoiI2FhYWEzMyIsImFycm93aGVhZENvbG9yIjoiIzMzMzMzMyIsImZvbnRGYW1pbHkiOiJcInRyZWJ1Y2hldCBtc1wiLCB2ZXJkYW5hLCBhcmlhbCIsImZvbnRTaXplIjoiMzJweCIsImxhYmVsQmFja2dyb3VuZCI6IiNlOGU4ZTgiLCJub2RlQmtnIjoiI0VDRUNGRiIsIm5vZGVCb3JkZXIiOiIjOTM3MERCIiwiY2x1c3RlckJrZyI6IiNmZmZmZGUiLCJjbHVzdGVyQm9yZGVyIjoiI2FhYWEzMyIsImRlZmF1bHRMaW5rQ29sb3IiOiIjMzMzMzMzIiwidGl0bGVDb2xvciI6IiMzMzMiLCJlZGdlTGFiZWxCYWNrZ3JvdW5kIjoiI2U4ZThlOCIsImFjdG9yQm9yZGVyIjoiaHNsKDI1OS42MjYxNjgyMjQzLCA1OS43NzY1MzYzMTI4JSwgODcuOTAxOTYwNzg0MyUpIiwiYWN0b3JCa2ciOiIjRUNFQ0ZGIiwiYWN0b3JUZXh0Q29sb3IiOiJibGFjayIsImFjdG9yTGluZUNvbG9yIjoiZ3JleSIsInNpZ25hbENvbG9yIjoiIzMzMyIsInNpZ25hbFRleHRDb2xvciI6IiMzMzMiLCJsYWJlbEJveEJrZ0NvbG9yIjoiI0VDRUNGRiIsImxhYmVsQm94Qm9yZGVyQ29sb3IiOiJoc2woMjU5LjYyNjE2ODIyNDMsIDU5Ljc3NjUzNjMxMjglLCA4Ny45MDE5NjA3ODQzJSkiLCJsYWJlbFRleHRDb2xvciI6ImJsYWNrIiwibG9vcFRleHRDb2xvciI6ImJsYWNrIiwibm90ZUJvcmRlckNvbG9yIjoiI2FhYWEzMyIsIm5vdGVCa2dDb2xvciI6IiNmZmY1YWQiLCJub3RlVGV4dENvbG9yIjoiYmxhY2siLCJhY3RpdmF0aW9uQm9yZGVyQ29sb3IiOiIjNjY2IiwiYWN0aXZhdGlvbkJrZ0NvbG9yIjoiI2Y0ZjRmNCIsInNlcXVlbmNlTnVtYmVyQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvciI6InJnYmEoMTAyLCAxMDIsIDI1NSwgMC40OSkiLCJhbHRTZWN0aW9uQmtnQ29sb3IiOiJ3aGl0ZSIsInNlY3Rpb25Ca2dDb2xvcjIiOiIjZmZmNDAwIiwidGFza0JvcmRlckNvbG9yIjoiIzUzNGZiYyIsInRhc2tCa2dDb2xvciI6IiM4YTkwZGQiLCJ0YXNrVGV4dExpZ2h0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0Q29sb3IiOiJ3aGl0ZSIsInRhc2tUZXh0RGFya0NvbG9yIjoiYmxhY2siLCJ0YXNrVGV4dE91dHNpZGVDb2xvciI6ImJsYWNrIiwidGFza1RleHRDbGlja2FibGVDb2xvciI6IiMwMDMxNjMiLCJhY3RpdmVUYXNrQm9yZGVyQ29sb3IiOiIjNTM0ZmJjIiwiYWN0aXZlVGFza0JrZ0NvbG9yIjoiI2JmYzdmZiIsImdyaWRDb2xvciI6ImxpZ2h0Z3JleSIsImRvbmVUYXNrQmtnQ29sb3IiOiJsaWdodGdyZXkiLCJkb25lVGFza0JvcmRlckNvbG9yIjoiZ3JleSIsImNyaXRCb3JkZXJDb2xvciI6IiNmZjg4ODgiLCJjcml0QmtnQ29sb3IiOiJyZWQiLCJ0b2RheUxpbmVDb2xvciI6InJlZCIsImxhYmVsQ29sb3IiOiJibGFjayIsImVycm9yQmtnQ29sb3IiOiIjNTUyMjIyIiwiZXJyb3JUZXh0Q29sb3IiOiIjNTUyMjIyIiwiY2xhc3NUZXh0IjoiIzEzMTMwMCIsImZpbGxUeXBlMCI6IiNFQ0VDRkYiLCJmaWxsVHlwZTEiOiIjZmZmZmRlIiwiZmlsbFR5cGUyIjoiaHNsKDMwNCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGUzIjoiaHNsKDEyNCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIiwiZmlsbFR5cGU0IjoiaHNsKDE3NiwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU1IjoiaHNsKC00LCAxMDAlLCA5My41Mjk0MTE3NjQ3JSkiLCJmaWxsVHlwZTYiOiJoc2woOCwgMTAwJSwgOTYuMjc0NTA5ODAzOSUpIiwiZmlsbFR5cGU3IjoiaHNsKDE4OCwgMTAwJSwgOTMuNTI5NDExNzY0NyUpIn19LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)


# 29. Динамические объекты и объекты с динамическими полями в консольном режиме Delphi. Примеры. 

```pascal
var 
    a: TRoom; {объект А класса TRoom}
    b: array[1..5] of TRoom;  {массив объектов типа TRoom}

type pTRoom=^TRoom;  {тип указателя на объекты класса TRoom}

var  pC: pTRoom;  {указатель на объекта класса TRoom}
```

Для динамического объекта необходимо выделить память:
```pascal
new(pC);
```
, а после его использования -- освободить память:
```pascal
dispose(pC);
```

Обращение к полям и методам аналогично доступу к полям записей:
Примеры:
```pascal
v := a.length;
s := a.square;
s := s + b[i].square;
pC^.length := 3;
```

### Создание полиморфных объектов:

Функция `new(<тип_указателя>)` -- возвращает адрес размещенного и, возможно, сконструированного объекта. После необходим вызов конструктора.
Или `new(<тип_указателя>, <конструктор>)`.

**Деструктор** -- метод класса, который используется для корректного уничтожения полиморфного объекта, содержащего невидимое поле. Деструктор можно переопределять.

### Уничтожение полиморфных объектов

Процедура `dispose(<указатель>)` -- освобождает память, на которую указывает указатель. Перед вызовом процедуры необходим вызов деструктора, если он указан, и затем -- выполняется освобождение памяти.
Или `dispose(<указатель>, <деконструктор>)`.

```pascal
program Ex_7_08;

{$APPTYPE CONSOLE}
uses
    SysUtils;

type
    pTRoomD = ^TRoomD;

    TRoomD = object
        length, width: Single;
        function square(): Single; virtual;
        constructor init(l, w: Single);
        destructor done;
    end;

type
    pTVRoomD = ^TVRoomD;
    TVRoomD = object(TRoomD)
        height: Single;
        function square(): Single; virtual;
        constructor init(l, w, h: Single);
    end;

function TRoomD.square;
begin
    result := length * width;
end;

constructor TRoomD.init;
begin
    length := l;
    width := w;
end;

destructor TRoomD.done;
begin
end;

constructor TVRoomD.init;
begin
    inherited init(l, w);
    height := h;
end;

function TVRoomD.square;
begin
    result := 2 * (inherited square() + height * (length + width));
end;

var
    pA: pTRoomD;
    pB: pTVRoomD;

begin
    {указатель базового типа, объект базового типа}
    pA := new(pTRoomD);
    pA^.init(3.5, 5.1);
    writeLn('Square =', pA^.square():6:2);  // `Square = 17.85`
    pA^.done();
    dispose(pA);

    {указатель производного типа, объект производного типа}
    pB := new(pTVRoomD);
    pB^.init(3.5, 5.1, 2.7);
    writeLn('Square =', pB^.square():6:2);  // `Square = 82.14`
    Dispose(pB, done);

    {указатель базового типа, объект производного типа}
    pA := new(pTVRoomD, init(3.5, 5.1, 2.7));
    writeLn('Square =', pA^.square():6:2);  // `Square = 82.14`
    dispose(pA, done);

    readLn;
end.
```

### Динамические поля в объектах

```pascal
program Ex_7_09;

{$APPTYPE CONSOLE}
uses
    SysUtils;

type
    pTRoomD = ^TRoomD;

    TRoomD = object
        length, width: Single;
        function square(): Single; virtual;
        constructor init(l, w: Single);
        destructor done; virtual;
    end;

type
    pTBRoomD = ^TBRoomD;

    TBRoomD = object(TRoomD)
        pB: pTRoomD;
        function square: Single; virtual;
        function BSquare: Single;
        constructor init(l, w: Single; lb, wb: Single);
        destructor done; virtual;
    end;

function TRoomD.square;
begin
    square := length * width;
end;

constructor TRoomD.init;
begin
    length := l;
    width := w;
end;

destructor TRoomD.done;
begin
end;

constructor TBRoomD.init;
begin
    inherited init(l, w);
    if (lb = 0) or (wb = 0) then
        pB := nil
    else
        pB := new(pTRoomD, init(lb, wb));
end;

function TBRoomD.BSquare;
begin
    if pB <> nil then
        BSquare := pB^.square
    else
        BSquare := 0;
end;

function TBRoomD.square;
begin
    square := inherited square() + BSquare();
end;

destructor TBRoomD.done;
begin
    if pB <> nil then
        Dispose(pB, done);
end;

var
    A: TBRoomD;
    pB1: pTBRoomD;
    pB2: pTRoomD;

begin
    {статический объект с динамическим полем}
    A.init(3.2, 5.1, 2.5, 1);
    writeLn(A.Square():6:2, A.BSquare():6:2);                // ` 18.82  2.50`
    A.done;
    
    {динамический полиморфный объект с динамическим полем}
    pB1 := new(pTBRoomD, init(3.2, 5.1, 2.5, 1));
    writeLn(pB1^.square():6:2, pB1^.BSquare():6:2);          // ` 18.82  2.50`
    dispose(pB1, Done);
    
    {динамический полиморфный объект с динамическим полем}
    pB2 := new(pTBRoomD, init(3.2, 5.1, 2.5, 1));
    writeLn(pB2^.square:6:2, pTBRoomD(pB2)^.BSquare():6:2);  // ` 18.82  2.50`
    dispose(pB2, done);
    
    readLn;
end.
```

# 30. Технология событийного программирования. События Windows, сообщения и события Delphi. Основные события Delphi. Примеры.

***Приложение** (в отличие от программы)* -- набор подпрограмм, вызываемых при наступлении некоторого события, которым считается любое изменение в системе, касающееся данного приложения.

## События Delphi и их обработчики

Обработчики сообщений *Windows* предусмотрены у объектов класса `TForm` и классов управляющих компонентов, таких как кнопки, редакторы и т. п.

Обработка выполняется следующим образом:
1. В системе происходит событие, например, пользователь передвинул мышь или нажал на клавишу клавиатуры, в результате генерируется сообщение об этом событии -- ***сообщение Windows***.
2. Сообщение *Windows* диспетчируется конкретному приложению.
3. В приложении сообщение передается активному компоненту (окну или управляющему элементу).
4. Метод обработки сообщения *Windows* компонента инициирует заранее предусмотренные ***события Delphi***.
5. Если в приложении предусмотрен соответствующий обработчик события *Delphi*, то он вызывается, если нет -- то продолжается обработка сообщения *Windows*.

### События *Delphi*

Обработчики сообщений *Windows*, встроенные в классы компонентов VCL, инициируют множество событий *Delphi*.

Например, обработчик события клавиатуры `WM_CHAR` класса `TForm` инициирует три события **Delphi**.

![enter image description here](https://i.imgur.com/ZmOBN8n.png)

### Обработчики событий Delphi

Для каждого обработчика событий предусмотрен заголовок и определённый список передаваемых ему параметров.
`procedure <компонент>.<Имя_компонента><Имя_события_delphi>(Sender: TObject[, {...}]);`

1. `procedure TForm1.FormActivate(Sender:TObject);`
   Параметр `Sender` -- отправитель (инициатор события).
2. `procedure TForm1.Edit1KeyPress(Sender: TObject; var Key: Char);`
   Параметр Key -- символ ANSI.
3. `procedure TForm1.Edit1KeyDown(Sender: TObject; var Key: Word; Shift: TShiftState);`
   Параметры: Key -- виртуальный код, Shift -- управляющие клав.
4. `procedure TForm1.Edit1KeyUp(Sender: TObject; var Key: Word; Shift: TShiftState);`

## Примеры событий Delphi, обрабатываемые объектами класса *TForm*
1. при изменении состояния формы:
   * `OnCreate` -- в начальной стадии создания формы - используется при необходимости задания параметров (цвет или размер);
   * `OnActivate` -- при получении формой фокуса ввода (окно становится активным и ему адресуется весь ввод с клавиатуры);
   * `OnShow` -- когда форма (окно) становится видимой;
   * `OnPaint` -- при необходимости нарисовать или перерисовать форму;
   * `OnResize` - при изменении размеров формы на экране;
   * `OnDeactivate` -- при потере формой фокуса ввода (окно становится неактивным);
   * `OnHide` -- при удалении формы с экрана (окно становится невидимым);
   * `OnCloseQuery` -- при попытке закрыть форму - обычно используется для создания запроса-подтверждения необходимости закрытия окна;
   * `OnClose` -- при закрытии формы;
   * `OnDestroy` -- при уничтожении формы;

2. от клавиатуры и мыши:
   * `OnKeyPressed` -- при нажатии клавиш, которым соответствует код ANSI;
   * `OnKeyDown`, `OnKeyUp` -- при нажатии и отпускании любых клавиш;
   * `OnClick`, `OnDblClick` -- при обычном и двойном нажатии клавиш мыши;
   * `OnMouseMove` -- при перемещении мыши (многократно);
   * `OnMouseDown`, `OnMouseUp` -- при нажатии и отпускании клавиш мыши;

3. при перетаскивании объекта мышью:
   * `OnDragDrop` -- в момент опускания объекта на форму;
   * `OnDragOver` -- в процессе перетаскивания объекта над формой (многократно);

4. другие:
   * `OnHelp` -- при вызове подсказки;
   * `OnChange` -- при изменении содержимого компонент.

