Виконала: Кочан Іванна Романівна
Лабраторна робота №1 (3 варіант 1 рівень)
Дано відсортований масив цілих чисел `nums` за зростанням (від менших до більших значень). Напишіть функцію, яка повертає новий масив, в якому кожен елемент є квадратом відповідного елемента з масиву `nums`. Отриманий масив також повинен бути відсортованим за зростанням.
​
Поверніть новий масив відповідно до вхідних даних.
​
Вхідні дані: nums = [-4,-2,0,1,3]
Результат: [0,1,4,9,16]
​
Вхідні дані: nums = [1,2,3,4,5]
Результат: [1,4,9,16,25]
​
Для перевірки виконання роботи реалізованого алгоритму слід використати бібліотеку `unittest` та перевірити роботу вашої функції на прикладах, наведених вище

Лабораторна робота №2 (3 варіант 3 рівень)
Фермер Джон побудував новий довгий загін для худоби, з N (2 <= N <= 100,000) секцій. Секції розташовуються уздовж прямої лінії в положеннях x1, ..., xN (0 <= x-i <= 1 000 000 000).
​
Його C (2 <= C <= N) корів не люблять нову будівлю і стають агресивними одна до одної, коли вони поставлені в сусідні стійла. Щоб уникнути ситуації, коли корови можуть заподіяти шкоду одна одній, фермер хоче розташувати агресивних корів у стійлах таким чином, щоб мінімальна відстань між будь-якими з них була настільки великою, наскільки це можливо. Яка найбільша мінімальна відстань?
​
​
Вхідні дані функції:  
N = 5
С = 3  
free_sections = `[1, 2, 8, 4, 9]
​
Результат
3
​
Пояснення: 
У фермера є 5 корів, з яких 3 агресивні. Їх можна роташувати в стійлах 1, 4 та 8 або 1,4, 9. Таким чином мінімальне значення максимальної дистанції становить 3
​
Підказка:
​
Оскільки у нас є щонайменше дві корови, найкраще, що ми можемо зробити, це розташувати їх у загоні у першому вільному стійлі і в кінці
​
Для перевірки виконання роботи реалізованого алгоритму слід використати бібліотеку `unittest` та перевірити роботу вашої функції на прикладах, наведених вище

Лабораторна робота №3 (3 варіант 3 рівень)
Для заданого бінарного дерева реалізуйте функцію, яка обчислює та повертає значення максимального діаметра у бінарному дереві - найвіддаленішу відстань між двома листками. Максимальний діаметр у бінарному дереві визначає найбільшу відстань між будь-якою парою листків (кінцевих вузлів) у дереві. Діаметр вимірюється як кількість ребер, які потрібно пройти, щоб дістатися одного листка від іншого. Максимальний діаметр не обов'язково має включати в себе кореневий вузол

Нехай у вас задане бінарне дерево такого вигляду:
        1
       /  \
      3    2
     / \
    7   4
   /     \
  8       5
 /         \
9           6
Для даного дерева максимальний діаметр становить 6: 9 -> 8 -> 7 -> 3 -> 4 -> 5 -> 6 - для проходження від листка 9 до листка 6 слід пройти 6 ребер.

Реалізована вами функція binary_tree_diameter(tree: BinaryTree) -> int отримує на вхід корінь бінарного дерева та повертає максимальний діаметр дерева.

Клас, який описує бінарне дерево (та будь який вузол дерева) має вигляд:
class BinaryTree:
    def __init__(self, value, left=None, right=None):
        self.value = value
        self.left = left
        self.right = right
Реалізація даної задачі не вимагає написання коду вставки чи виділення елементів з бінарного дерева. У тесті ви можете створити достатню кількість елементів класу BinaryTree наступним чином:

root = BinaryTree(3)
root.left = BinaryTree(9)
root.right = BinaryTree(20)

Лабраторна робота №5 (3 варіант 3 рівень)
Для всіх задач слід написати тести з використанням бібліотеки unittest. Ваш проект має бути розділено на окремі папки для коду додатку та тестів (src та test відповідно).

При написанні коду дотримуйтесь стандарту PEP 8, який визначає правила форматування Python-коду, такі як відступи, довжина рядків, іменування змінних тощо. Для полегшення читабельності коду слід відформатувати ваш код з допомогою Black
Критично важливим є постачання газу між сховищами та містами пінгвінів взимку. Вибух газопроводів може призвести до дефіциту палива та викликати значні проблеми у домівках бравих пінгвінів. Тому ряд газопроводів зараз відключили для ремонту.

Ви, як студент курсу Алгоритми і структури даних маєте бажання допомогти Пінгвінам. Ви готові написати для них алгоритм, який перевірить, чи існує спосіб транспортування палива з будь-якого сховища до будь якого міста з використанням газопроводів, які не вивели в ремонт. Зауважте, що газ по трубі можна транспортувати лише в одному напрямку.

Для розв'язання цієї задачі пінгвіни надали вам:

список міст

список газосховищ

список активних газопроводів, у форматі [ ['Львів', 'Стрий'], ['Долина', 'Львів'], ['Сховище_1', 'Сховище_2'] ], де ['Львів', 'Стрий'] означає наявність газопроводу між містами Львів та Стрий, де подача газу відбувається від Львова до Стрия

Ваша програма має повернути результат у форматі: [ 'газосховище', ['місто_1', 'місто_2'] , де:

газосховище - назва газосховища
['місто_1', 'місто_2'] - список міст, до яких неможливо подати газ з цього газосховища
Зауважте, що газ може подаватись з газосховища до будь якого міста транзитом через інші міста.

У випадку, якщо є зв'язок між усіма газосховищами та містами, поверніть пустий список

