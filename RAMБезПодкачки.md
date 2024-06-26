# Методы распределения оперативной памяти без использования внешней памяти.

## Одинаковые фиксированные разделы
**Плюсы:** Очень быстро искать нужный блок памяти. Можно сразу зарезервировать PIDы, нет проблемы с защитой (если старшие биты совпадают, то имеешь доступ)
**Минусы:** Неоптимальный расход памяти или нехватка памяти на крупные процессы.

## Различные фиксированный разделы
Размеры - степени двойки, количество - тоже
Добавляем многоуровневые очереди с возможностью перехода.

**Минусы:** Невозможно предсказать сколько потребуется памяти - в итоге она может неравномерно распределяться
**Плюсы:** Всё ещё быстрый поиск

## Динамические адреса
Теперь процессы не могут просить больше памяти, чем дали изначально

**Плюсы:** Более оптимально расходуется память.
**Минусы:** Поиск через суммирование размеров - долго, фрагментированность памяти.