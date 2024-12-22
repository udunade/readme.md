# Проектное задание. Дмитриева Арина Сергеевна Ф-2346
## Название программы "Личный финансовый учет"
### Ссылка на Google.Colab: https://colab.research.google.com/drive/1ugbEieml-Jpvw8tZXx2AFxabFM5uFtIv?usp=sharing
#### Видео: https://drive.google.com/drive/folders/12acXXDN9cc8nA9pScgS4V5X9FL0990xF?usp=sharing
#### Пояснения работы программы:
- Программа создает объект FinanceTracker, который хранит текущий баланс и список транзакций.
- Пользователь может добавить доходы или расходы, и программа автоматически обновит баланс.
- История транзакций хранится в виде списка и отображается по запросу.
- Ввод данных обрабатывается с проверкой на корректность.
#### Основные компоненты:
1. _Класс FinanceTracker:_
  * Конструктор __init__: Инициализирует переменные экземпляра balance (баланс) и transactions (список транзакций) с начальными значениями 0 и пустой список соответственно.
  * Метод add_income: Добавляет указанную сумму к балансу и записывает транзакцию в список транзакций.
  * Метод add_expense: Вычитает указанную сумму из баланса и записывает транзакцию в список транзакций.
  * Метод display_balance: Выводит текущий баланс с двумя знаками после запятой.
  * Метод display_transactions: Выводит историю транзакций, если она есть, или сообщение о том, что история пуста.
2. _Функция main:_
  * Основной цикл: Бесконечный цикл, который предлагает пользователю выбрать одну из пяти команд:
    1. Добавить доход
    2. Добавить расход
    3. Посмотреть баланс
    4. Посмотреть историю транзакций
    5. Выйти
  * Обработка команд: В зависимости от выбранной команды, программа выполняет соответствующие действия:
    1. Команда 1 (Добавить доход): Пользователь вводит сумму дохода, которая проверяется на положительность. Если сумма корректна, метод add_income добавляет сумму к балансу и отображает сообщение.
    2. Команда 2 (Добавить расход): Аналогично команде 1, но сумма вычитается из баланса.
    3. Команды 3 и 4 (Посмотреть баланс и историю транзакций): Вызывают соответствующие методы для отображения информации.
    4. Команда 5 (Выйти): Завершает программу.
    5. Обработка некорректного ввода: Если пользователь вводит что-то кроме чисел для суммы, программа сообщает об ошибке и просит ввести корректное число.
