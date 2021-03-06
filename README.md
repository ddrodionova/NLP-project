# **Добро пожаловать в поисковой корпус стихов о животных!** :cat:

> Код требует наличие модуля `thisapidoesnotexist`. Вы можете скачать его с помощью `pip install thisapidoesnotexist`.

[Здесь](/codes) можно найти две тетрадки с кодом. 
1. [`make_db.ipynb`](/codes/make_db.ipynb) код, который собирает нужные данные и создаёт корпус стихов. 
2. [`сorpus_search.ipynb`](/codes/corpus_search.ipynb) код, который осуществляет поиск по корпусу. 

[`База данных`](https://drive.google.com/file/d/1BmnwmUATSQxeTMt4f3gfv5mkTX76UaOA/view?usp=sharing)

## **Данные**
Тексты корпуса взяты с сайта https://rustih.ru из раздела "Стихи про животных".
## **Обработка**
Тексты были поделены на предложения, затем лемматизированы и рамечены по частям речи с помощью анализатора Mystem. Затем данные были закачены в базу данных, по которой дальше происходит поиск.

## **Поиск**
Поисковая система корпуса позволяет задавать запросы состоящие из одного, двух или трёх слов, каждый из которых может быть задан как: 

*   Лемма
*   Слово в конкретной форме 

    *   Для этого напишите его в двойных кавычках: "*ваше слово*" 
*   Тег части речи
    * Для этого напишите обозначение части речи (из списка ниже) 
*   Лемма/словоформа и часть речи
    * Для этого напишите слитно с ним '+' и часть речи (из списка ниже): *ваше слово*+POS или "*ваше слово*"+POS

### **Список частей речи**

Обозначение | Расшифровка
-|-
A	| прилагательное
ADV |	наречие
ADVPRO |	местоименное наречие
ANUM |	числительное-прилагательное
APRO |	местоимение-прилагательное
COM	| часть композита - сложного слова
CONJ |	союз
INTJ |	междометие
NUM	|числительное
PART |	частица
PR |	предлог
S	|существительное
SPRO |	местоимение-существительное
V	|глагол

## **Примеры запросов**


```
search('волк')
search('"щенок"')
search('ADV')
search('"щенка"+S')
search('спать+V')

И все их возможные комбинации длиной от 1 до 3
```
