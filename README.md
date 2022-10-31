## Общи задачи

### Разглеждаме свързан списък представен по следния начин
template <class G>
struct Node {
    G key;
    Node<G>* next;
    Node(G key) : key(key), next(nullptr){};
};

#### L1 и L2 са свързани списъци, като елементите в тях са сортирани лексикографски. Да се реализира функция unionList, която да приема L1 и L2 като списъци и връща нов списък чийто елементи са същите от L1 и L2, сортирани лексикографски.

#### Node<G>*  toList(const int* arr, size_t size)
Получава указател към масив arr съдържащ size елемента и по него създава и връща свързан списък. Списъкът да има същите стойности като тези в масива, подредени в същия ред. Паметта за кутиите на списъка да се заделя с new.

#### void deleteList(Node<G>* lst)
Освобождава (с delete) паметта заета от списъка lst.

#### void removeConsecutiveDuplicates(Node<G>* lst)
Премахва всички последователни повторения на елементи от списъка lst. Премахнатите елементи да се унищожават с delete. Например, нека е дадена редицата:
1, 1, 2, 2, 1, 1, 2, 2, 2, 2, 1, 2, 1, 2
След премахване на последователните повторения от нея ще останат само:
1, 2, 1, 2, 1, 2, 1, 2



### https://docs.google.com/document/d/16ZRgs2kk-KDxv5kt8IOdtQDW_cWyd_YK5oBcWAewjVg/edit

## Трябва да напишете система за настаняване на клиенти в бар Мраз. В заведението има само един бар за сядане, където всички места са номерирани последователно от 1 до N. На всяко място в бара има кранче за някои (не задължително всички) от напитките, които се предлагат: бира, водка, уиски, текила, кола, ром, джин и мента. Вашата задача е да настанявате групи пристигащи клиенти при следните условия:

клиентите от всяка група трябва да останат в същият ред, в който са дошли;
клиентите от всяка група може да сядат на максимум 5 места един от друг. Помежду им може да има други клиенти;
всеки клиент иска да пие някои от напитките и може да бъде настанен само на място, на което има всички напитки, които той иска.
В задачата не можете да използвате алгоритми и структури от данни от STL.

а) (10 т) Напишете функция, която приема като аргумент едносвързан списък описващ местата в бара и двусвързан списък, който описва групата клиенти. В бара може да има вече настанени клиенти. Ако е невъзможно да се настани новата група, функцията трябва да върне грешка. Използвайте следният прототип (сами преценете какви членове да има в структурите, но прототипът не може да се променя):

struct BarSlot;
struct Client;
bool place(BarSlot *bar, Client *clients);
б) (2 т) Освен това, напишете и функция, която приема описание на бар в едносвързан списък, и масив от групи от клиенти. Функцията трябва да провери дали всички групи от клиенти могат да бъдат настанени в някакъв ред. Използвайте следният прототип:

bool placeAll(BarSlot *bar, Client **groups, int groupCount);
Не е нужно да имплементирате пълни класове за контейнери. Възможно е нещата да се направят така, че дадените прототипи да приемат директно указател към възел в списък.

в) (3 т) Демонстрирайте функцията в програма, която прочита данните за бара и групите клиенти от клавиатурата, записва ги в съответните структури от данни и опитва да ги настани. След това извежда на екрана резултата от настаняването и кои групи не могат да бъдат настанени.
