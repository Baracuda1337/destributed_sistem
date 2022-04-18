# **Лабораторна робота №2**

-----------------------------------
## Необхідні ресурси:
- Встановлений компілятор для Python.

## Інформація про програму:
- Виводить в терміналі "Hello World!".
- Виконує команди: ping, echo, login, list, msg, file, exit.

## Опис Команд:
### 1. Команда `ping <Address: String>`.
#### Ця команда перевіряє зєднання з сервером, сайтом чи будь-яким іншим пристроєм за вказаною IP або DNS адресою. Дані команді передається тільки один параметр - `<Address: String>`
#### Результатом виконання у разі успішного зєднання в першому рядку записується `Ping <Address: String> ...` і в наступному рядку `Ping <Address: String> request success.`.
#### Якщо ж кількість введених параметрів не буде рівна "1", то замість результату виводиться повідомлення з описом помилки в дужках`PING ERROR (Incorect input argument)`

### Приклад виконання команди:
```text
Hello World!
========================================
Input Command: ping
Entered command = "ping", parameters = []
----------------------------------------

Results:
PING ERROR (Incorect input argument)
========================================
Input Command: ping 192.168.1.1
Entered command = "ping", parameters = ['192.168.1.1']
----------------------------------------

Results:
Ping 192.168.1.1 ...
Ping 192.168.1.1 request success.

```

### 2. Команда `echo <anyText: String> <anyText: String> ...`.
#### Ця команда виводить на екрані текст з вхідних параметрів - `<anyText: String>`. Ця команда може отримувати будь-яку кількість параметрів. Кожний параметр відображається в новому рядку.

### Приклад виконання команди:
```text

Hello World!
========================================
Input Command: echo Pavlo
Entered command = "echo", parameters = ['Pavlo']
----------------------------------------

Results:
Pavlo
========================================
Input Command: echo Petro "L a m p a"
Entered command = "echo", parameters = ['Petro', 'L a m p a']
----------------------------------------

Results:
Petro
L a m p a

```

### 3. Команда `login <login: String> <password: String>`.
#### Ця команда дозволяє користувачу залогінитися. Дані команді передається два параметри - `<login: String>` і `<password: String>`.
#### Результатом виконання команди буде:
- Якщо логін даного користувача немає в базі даних, то в консолі виводиться `LOGIN ERROR (Incorect input login or password)`.
- Якщо логін даного користувача є в базі даних, але відповідний до нього пароль введений неправильно, то в консолі виводиться `LOGIN ERROR (Incorect input login or password)`.
- Якщо логін даного користувача є в базі даних, і відповідний до нього пароль введений правильно, то в першому рядку консолі виводиться - `LOGIN SUCCESS:`, а в наступному рядку - `Hello, <nameUsers: String>`.
- Якщо кількість введених параметрів не дорівнює 2, то в консолі виводиться `LOGIN ERROR (Incorect input argument)`.

### Приклад виконання команди:
```text
Input Command: login
Entered command = "login", parameters = []
----------------------------------------

Results:
LOGIN ERROR (Incorect input argument)
========================================
Input Command: login Pavlo22_std std22
Entered command = "login", parameters = ['Pavlo22_std', 'std22']
----------------------------------------

Results:
LOGIN SUCCESS:
 Hello, Pavlo22
========================================
Input Command: login Pavlo22 sd2
Entered command = "login", parameters = ['Pavlo22', 'sd2']
----------------------------------------

Results:
LOGIN ERROR (Incorect input login or password)
```

### 4. Команда `list`.
#### Ця команда виводить на екран список назв всіх зареєстрованих користувачів які знаходяться в базі даних. Для цієї команди не потрібно вводити параметри, якщо було введено параметри то вони ігноруються. Назва кожного користувача відображається в новому рядку з його поряковим номером - `<№Users: Int>. <nameUsers: String>` .
#### База даних:
-user_names = ['Pavlo22', 'Petro33', 'Sergiy44', 'Ivan55']
-user_logins = ['Pavlo22_std', 'Petro33_std', 'Sergiy44_std', 'Ivan55_std']
-user_passwords = ['std22', 'std33', 'std44', 'std55']
### Приклад виконання команди:
```text
========================================
input Command: list
Entered command = "list", parameters = []
----------------------------------------

Results:
1. Pavlo22
2. Petro33
3. Sergiy44
4. Ivan55
========================================
```

### 5. Команда `msg <destinationUser: String> <text: String>`.
#### Ця команда надсилає текстове повідомлення іншому користувачу. Дані команді передається два параметри - `<destinationUser: String>` і ` <text: String>`.
#### Результатом виконання команди буде:
- Якщо назви даного користувача немає в базі даних, то в консолі виводиться `MESSAGE SENDING ERROR (This user not found)`.
- Якщо назва даного користувача є в базі даних, то в консолі виводиться `MESSAGE SENDING SUCCESS`.
- Якщо кількість введених параметрів не дорівнює 2, то в консолі виводиться `MESSAGE SENDING ERROR (Incorect input argument)`.

### Приклад виконання команди:
```text
Input Command: msg Pavlo22 Hi
Entered command = "msg", parameters = ['Pavlo22', 'Hi']
----------------------------------------

Results:
MESSAGE SENDING SUCCESS
========================================

```

### 6. Команда `file <destinationUser: String> <filename: String>`.
#### Ця команда надсилає файлове повідомлення іншому користувачу. Дані команді передається два параметри - `<destinationUser: String>` і ` <filename: String>`.
#### Результатом виконання команди буде:
- Якщо назви даного користувача немає в базі даних, то в консолі виводиться `FILE SENDING ERROR (User not found)`.
- Якщо назва даного користувача є в базі даних, але даного файлу немає, то в консолі виводиться `FILE SENDING ERROR (File not found)`.
- Якщо назва даного користувача є в базі даних, і цей файл існує, то в консолі виводиться `FILE SENDING SUCCESS`.
- Якщо кількість введених параметрів не дорівнює 2, то в консолі виводиться `FILE SENDING ERROR (Incorect input argument)`.

### Приклад виконання команди:
```text
Input Command: file Pavlo22 lab2.py
Entered command = "file", parameters = ['Pavlo22', 'lab2.py']
----------------------------------------

Results:
FILE SENDING SUCCESS
========================================
Input Command: file Pavlo22 C:\Users\Павел\Deskto\Лабораторна_Cisco_№1_з_Розподілені_ІКС.DOCX
Entered command = "file", parameters = ['Pavlo22', 'C:\\Users\\Павел\\Deskto\\Лабораторна_Cisco_№1_з_Розподілені_ІКС.DOCX']
----------------------------------------

Results:
FILE SENDING ERROR (File not found)
========================================
```

### 7. Команда `exit`.
#### Ця команда виходить з циклу для опитування введення команд. Для цієї команди не потрібно вводити параметри, якщо було введено параметри то вони ігноруються.
- Результатом виконання команди буде - `Exit from cycle`

### Приклад виконання команди:
```text
nput Command: exit
Entered command = "exit", parameters = []
----------------------------------------

Results:
Exit from cycle


Input Command: list
Entered command = "list", parameters = []
----------------------------------------

Results:
1. Pavlo22
2. Petro33
3. Sergiy44
4. Ivan55
========================================

```
