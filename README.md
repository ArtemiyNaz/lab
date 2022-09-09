# Описание функции

```
def sort(list):
  for i in range(1, len(list)):
    num = list[i]
    j = i -1
    while j >= 0 and num < list[j]:
      list[j+1] = list[j]
      j -= 1
    list[j+1] = num
  return(list)
  
```

Поочереди берётся каждый эллемент списка, начиная со второго.  
Запоминаем этот эллемент.  
Задаём переменную для сравнения с нашим числом.  
Пока число слева от нашего больше или равно 0 и больше чем наше чесло, заменяем наше число справа на левое.  
Двигаемся влево.  
Записываем наше число на место того которое заменило его.  
И функция возвращает список(list).  

## Основная функция

```

start = monotonic()
list = []
for x in range(0, 9):
  list.append(random.randint(0, 9))
sort(list)
finish = monotonic()
print(round(finish - start, 4))

```

Часы начинаеют отчёт.  
Создаётся пустой список.  
Список заполняется случайными числами от 0 до 9.  
Вызывается функция.  
Часы останавливаются.  
Ищется разницу между концом и началом отчёта и выводиться на экран с 4-мя знаками после запятой.  

## Таблица 

|Кол-во эллементов|Время выполнения|
|:-:|:-:|
|100|0,0007|
|500|0.0197|
|1000|0.0777|
|2000|0.5108|
|4000|1.8639|
|6000|4.8022|
