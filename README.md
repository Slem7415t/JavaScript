# JavaScript
about:blank - при вводе в поле поиска в браузере вызывает пустую страницу.
console.log(); - вывод в консоль.
// - коментарий, /* */ - многострочный коментарий.
var, let - создание переменных.
const - создание констант.
= - присваивание.
.length - узнать длину строки.
пр: сторока[сторока.length-1] -узнать последний индекс строки или массива(строка и есть массив).
.slice(начальная позиция не вллючена, конечная позиция включительно) - позволяет выббрать из строки элементы.
пр: let str = 'Привет'
    console.log(str.slice(1, 3)); // ри
    console.log(str.slice(3)); // вет
.toLowerCase() - все в нижний регистр.
.toUpperCase() - все в верхний регистр.
.trim() - уберает лишнии пробелы.

&& и AND               || или OR        ! - отрицание

x y z                  x y z
0 0 0                  0 0 0
0 1 0      x+y=z       0 1 1      
1 0 0                  1 0 1
1 1 1                  1 1 1

undefined - не определена.
null - пустая.
`` - шаблонные литералы позволяют указывать текст на разных строчках и встраивать параменные.

Math.random() - случайное число от 0 до 1.
Math.max() - максимальное значение из всех, что переданы в скобках через запятую.
Math.pow() - возвести в степень, в скобках через запятую(чтоб извлечь корень, вторым числом передаем десятичную дробь).
Math.sqrt() - извлечь только квадратный корень, число в скобках.
Math.floor() - округляет число в меньшую сторону, передается в скобках.
Math.ceil() - округляет число в большую сторону, передается в скобках.
Math.round() - округляет число к ближайшему целому, передается в скобках.
Math.trunc() - округляет число отбрасыванием дробной части, передается в скобках.

.toFixed() - округляет число до определенного количества знаков после запятой, в скобках пишем до скольки знаков округлить.

Чтобы превратить строку в число перед ней надо поставить +
пр: let a = '5'
    console.log(a + 5); // 55
    console.log(+a + 5); // 10

function isNumber(n) {
  return !isNAN(parseFloat(n))&&!isNaN(n-0)
} - проверяет является ли значение числом

function randomInteger(max, min) {
    let rand = min + Math.random() * (max + 1 - min);
    return Math.floor(rand);
} - рандомное число от min до max.

## Массивы
let arr = [5, 2, "Hi", true]; - массив.
Индексы массива от 0, чтобы получить значение, указать имя массива и индекс.
пр: arr[2]; // Hi

let arr2 = [[1, 2, 3], [4, 7, 8], [9, 5, 6]]; - вложенный массив.
пр: arr2[1][2]; // 8
вложенностей может быть сколько угодно.

###очередь
.shift() - удаляет первый элемент массива
.push() - добавляет последний элемент массива

###стек
.push()
.pop() - удаляет из конца массива

.shift()
.unshift() - добавляет в начало массива

.concat - склеивает массивы
пр: arr.concat(arr2); // arrarr2 не портит исходные массивы
.indexOf() - получить индекс элемента, в скобках его значение.
.join() - объеденить элементы в строку, в скобках можно указать разделитель
.splice() - удаляет и добавляет в массив любые элементы
пр: .splice(с какого элемента начинаем не включая, сколько элементов удаляем, через запятую элементы которые добавляем необязательно);
- Поддерживает отритцательные значения, при них нумерация с конца массива.
.slice() - выводит элементы массива от и до, аргументы передаются в скобках.
- тоже поддерживает отритцательные значения.
.includes() - проверяет есть ли элемент в массиве, элемент пишем в скобках, возвращает true или false
.reverse() - возвращает массив с элементами в обратном порядке.
.split() - переводит строку в массив, внутри скобок в кавычках указывается разделитель.
Если применить к слову и указать разделитель, пустые кавычки, то получем массив из букв этого слова.

##Объект
let obj = {
    "color" : "Tomato",
    "numbers" : ["8888", "7777"],
    "checked" : true
} - объект
пр: obj["color"] // Tomato
или obj.color // Tomato
или obj.number[1] // 7777

Object.keys() - выводит массив из ключей объекта, в скобках название объекта.
название объекта["ключ"] = "значение"; - добавить в объект новую ключ пару

В объекте значения хранятся не под индексами как в массиве, а под ключами, потому что объект не отсортирова по порядку, выводиться в разнобой. Может как и объект состоять из массивов, так и массив состоять из объектов.
