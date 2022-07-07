# Коллекции для параллельной работы

## Задача 1 (обязательная)

Эта задача делается на основе предыдущей про красивые строки. Сделайте от того решения новую ветку `queue`.

Раньше вы сперва генерировали все строки, сохраняли их все в память и только после этого считали количество красивых.
Теперь вы хотите распараллелить этап создания строк и этапы анализа их красивости.
Для этого у вас строки будут генерироваться в отдельном потоке и заполнять блокирующие очереди, максимальный размер которых ограничьте в 100 строк.
Очереди нужно будет сделать по одной для каждого критерия, тк строка должна быть обработана каждым потоком, определяющим их красивость.

Подсказка: воспользуйтесь `ArrayBlockingQueue`.

## Задача 2 (необязательная)

Эта задача делается на основе [первой задачи про синхронизацию](../SYNC.md).
Отведите от вашего её решения новую ветку `multimap`.

Замените `HashMap` на потокобезопасную мапу, избавьтесь от лишней синхронизации.