# **����������� ������ �2**

-----------------------------------
## �������� �������:
- ������������ ��������� ��� Python.

## ���������� ��� ��������:
- �������� � ������� "Hello World!".
- ������ �������: ping, echo, login, list, msg, file, exit.

## ���� ������:
### 1. ������� `ping <Address: String>`.
#### �� ������� �������� ������� � ��������, ������ �� ����-���� ����� �������� �� �������� IP ��� DNS �������. ��� ������ ���������� ����� ���� �������� - `<Address: String>`
#### ����������� ��������� � ��� �������� ������� � ������� ����� ���������� `Ping <Address: String> ...` � � ���������� ����� `Ping <Address: String> request success.`.
#### ���� � ������� �������� ��������� �� ���� ���� "1", �� ������ ���������� ���������� ����������� � ������ ������� � ������`PING ERROR (Incorect input argument)`

### ������� ��������� �������:
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

### 2. ������� `echo <anyText: String> <anyText: String> ...`.
#### �� ������� �������� �� ����� ����� � ������� ��������� - `<anyText: String>`. �� ������� ���� ���������� ����-��� ������� ���������. ������ �������� ������������ � ������ �����.

### ������� ��������� �������:
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

### 3. ������� `login <login: String> <password: String>`.
#### �� ������� �������� ����������� �����������. ��� ������ ���������� ��� ��������� - `<login: String>` � `<password: String>`.
#### ����������� ��������� ������� ����:
- ���� ���� ������ ����������� ���� � ��� �����, �� � ������ ���������� `LOGIN ERROR (Incorect input login or password)`.
- ���� ���� ������ ����������� � � ��� �����, ��� ��������� �� ����� ������ �������� �����������, �� � ������ ���������� `LOGIN ERROR (Incorect input login or password)`.
- ���� ���� ������ ����������� � � ��� �����, � ��������� �� ����� ������ �������� ���������, �� � ������� ����� ������ ���������� - `LOGIN SUCCESS:`, � � ���������� ����� - `Hello, <nameUsers: String>`.
- ���� ������� �������� ��������� �� ������� 2, �� � ������ ���������� `LOGIN ERROR (Incorect input argument)`.

### ������� ��������� �������:
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

### 4. ������� `list`.
#### �� ������� �������� �� ����� ������ ���� ��� ������������� ������������ �� ����������� � ��� �����. ��� ���� ������� �� ������� ������� ���������, ���� ���� ������� ��������� �� ���� �����������. ����� ������� ����������� ������������ � ������ ����� � ���� ��������� ������� - `<�Users: Int>. <nameUsers: String>` .
#### ���� �����:
-user_names = ['Pavlo22', 'Petro33', 'Sergiy44', 'Ivan55']
-user_logins = ['Pavlo22_std', 'Petro33_std', 'Sergiy44_std', 'Ivan55_std']
-user_passwords = ['std22', 'std33', 'std44', 'std55']
### ������� ��������� �������:
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

### 5. ������� `msg <destinationUser: String> <text: String>`.
#### �� ������� ������� �������� ����������� ������ �����������. ��� ������ ���������� ��� ��������� - `<destinationUser: String>` � ` <text: String>`.
#### ����������� ��������� ������� ����:
- ���� ����� ������ ����������� ���� � ��� �����, �� � ������ ���������� `MESSAGE SENDING ERROR (This user not found)`.
- ���� ����� ������ ����������� � � ��� �����, �� � ������ ���������� `MESSAGE SENDING SUCCESS`.
- ���� ������� �������� ��������� �� ������� 2, �� � ������ ���������� `MESSAGE SENDING ERROR (Incorect input argument)`.

### ������� ��������� �������:
```text
Input Command: msg Pavlo22 Hi
Entered command = "msg", parameters = ['Pavlo22', 'Hi']
----------------------------------------

Results:
MESSAGE SENDING SUCCESS
========================================

```

### 6. ������� `file <destinationUser: String> <filename: String>`.
#### �� ������� ������� ������� ����������� ������ �����������. ��� ������ ���������� ��� ��������� - `<destinationUser: String>` � ` <filename: String>`.
#### ����������� ��������� ������� ����:
- ���� ����� ������ ����������� ���� � ��� �����, �� � ������ ���������� `FILE SENDING ERROR (User not found)`.
- ���� ����� ������ ����������� � � ��� �����, ��� ������ ����� ����, �� � ������ ���������� `FILE SENDING ERROR (File not found)`.
- ���� ����� ������ ����������� � � ��� �����, � ��� ���� ����, �� � ������ ���������� `FILE SENDING SUCCESS`.
- ���� ������� �������� ��������� �� ������� 2, �� � ������ ���������� `FILE SENDING ERROR (Incorect input argument)`.

### ������� ��������� �������:
```text
Input Command: file Pavlo22 lab2.py
Entered command = "file", parameters = ['Pavlo22', 'lab2.py']
----------------------------------------

Results:
FILE SENDING SUCCESS
========================================
Input Command: file Pavlo22 C:\Users\�����\Deskto\�����������_Cisco_�1_�_���������_���.DOCX
Entered command = "file", parameters = ['Pavlo22', 'C:\\Users\\�����\\Deskto\\�����������_Cisco_�1_�_���������_���.DOCX']
----------------------------------------

Results:
FILE SENDING ERROR (File not found)
========================================
```

### 7. ������� `exit`.
#### �� ������� �������� � ����� ��� ���������� �������� ������. ��� ���� ������� �� ������� ������� ���������, ���� ���� ������� ��������� �� ���� �����������.
- ����������� ��������� ������� ���� - `Exit from cycle`

### ������� ��������� �������:
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
