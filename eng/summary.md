# Конспект видео
*Автоматически сгенерировано с помощью AI 03.06.2025*

Этот документ представляет собой автоматически сгенерированный конспект видео, созданный с использованием искусственного интеллекта. Конспект содержит ключевые моменты, важные концепции и скриншоты из видео.

## Содержание

- [Часть 1: 00:00:00.000 - 00:23:16.040](#часть-1)
- [Часть 2: 00:23:16.040 - 00:50:12.460](#часть-2)
- [Часть 3: 00:50:12.460 - 01:15:08.680](#часть-3)
- [Часть 4: 01:15:10.680 - 01:38:44.200](#часть-4)
- [Часть 5: 01:38:44.200 - 02:06:12.420](#часть-5)
- [Часть 6: 02:06:12.420 - 02:34:40.060](#часть-6)
- [Часть 7: 02:34:40.060 - 02:58:01.220](#часть-7)
- [Часть 8: 02:58:01.220 - 03:26:19.760](#часть-8)
- [Часть 9: 03:26:19.760 - 03:50:16.160](#часть-9)
- [Часть 10: 03:50:16.160 - 03:53:56.980](#часть-10)

## Часть 1
*Таймкод: 00:00:00.000 - 00:23:16.040*

# Подготовка к демоэкзамену по VipNet: Введение и Организационные Моменты

## Введение

- Ведущий: Купин Андрей Владимирович
- Тема: Подготовка к демоэкзамену, разбор одного из вариантов задания, аналогичного основному экзамену
- Предоставлены ссылки на необходимые материалы:
  - Мануал по WebNet (Яндекс.Диск)
  - Образ WebNet for Linux (клиент для Linux)
  - Задание для подготовки к демоэкзамену
  - Программы WebNet (demo.iso)

---

## Состав ПО для демоэкзамена

- **AnyToISO** — конвертация папок в формат ISO для передачи ключей на координаторы
- **VipNet-администратор** — основной компонент для построения и управления сетью VipNet
- **VipNet SignForming** — информационный модуль
- **VipNet Publication Service, Registration Point** — не используются из-за отсутствия лицензий
- **VipNet-клиент** — создание VPN-сети на клиентских устройствах
- **SQL Server** — хранение базы данных VipNet
- **SQL Manager Studio** — возможно потребуется для работы с БД

**Важный момент для иллюстрации:**  
Показ demo.iso и состава ПО на экране — [00:03:00]

![Скриншот в 00:03:00](./screenshots\screenshot_00-03-00.jpg)
 (примерно, когда перечисляются программы).

---

## Организационные вопросы

- **Разрешение экрана:** Рекомендовано использовать 1920x1080 для лучшего качества трансляции
- **Доступ к материалам:** Все ссылки предоставлены в чате, включая архив с загрузочными файлами и методичку
- **Запись занятия:** Ведется запись, будет доступна после занятия

---

## Цифровая гигиена (важно для экзамена!)

- **Обязательные правила:**
  - Блокировка компьютера при уходе (Windows: Win+L, RDoS: Ctrl+Alt+L)
  - Организация рабочего места: отсутствие посторонних предметов и документов с конфиденциальной информацией на виду
  - По завершению экзамена — сложить все выданные материалы обратно, не оставлять пароли на виду
  - Задвигать стул при уходе
  - При необходимости выйти — поднять руку, заблокировать экран, аккуратно покинуть место

**Важный момент для иллюстрации:**  
Показ правильной организации рабочего места и блокировки экрана — [00:13:30]

![Скриншот в 00:13:30](./screenshots\screenshot_00-13-30.jpg)


---

## Обзор задания и структуры сети

- **Структура сети:**
  - Виртуальные машины: net1-админца (администратор), оперца (оператор), кордца (координатор/маршрутизатор)
  - Центральный офис и филиал, каждый с собственными сетями
- **Этапы создания защищённой сети VipNet:**
  1. Установка всех компонентов (координатор, клиенты, администратор)
  2. Создание топологии защищённой сети в VipNet-администраторе (виртуальные узлы/host'ы, группы безопасности, правила маршрутизации и доверия)
  3. Выпуск ключей (через удостоверяющий ключевой центр — УКЦ)
  4. Установка ключей на клиентские машины
  5. Тестирование сети

```plaintext
Основные этапы:
1. Создание топологии сети (ЦУС)
2. Выпуск ключей (УКЦ)
3. Установка ключей на клиенты
4. Тестирование сети
```

**Важный момент для иллюстрации:**  
Показ схемы сети и этапов настройки — [00:18:00]

![Скриншот в 00:18:00](./screenshots\screenshot_00-18-00.jpg)


---

## Краткое объяснение защищённой сети VipNet

- VipNet-сеть — виртуальная защищённая сеть, строится поверх обычной физической сети, использует шифрование для передачи данных
- Координаторы устанавливаются в каждом офисе, между ними создаётся защищённый канал
- Пользователи подключаются через VipNet-клиенты из любой точки мира
- Все данные между филиалами шифруются, перехват невозможен без расшифровки

---

## Пример IP-адресации для задания

- **Центральный офис:** 192.168.110.0/28
- **Филиал:** 10.10.10.0/26
- **Интернет для координаторов:** 108.18.10.0/20

**Важный момент для иллюстрации:**  
Показ схемы с IP-адресами — [00:21:30]

![Скриншот в 00:21:30](./screenshots\screenshot_00-21-30.jpg)


---

## Итоги

- Подготовлены все необходимые материалы и ПО для демоэкзамена
- Разъяснены организационные вопросы и правила цифровой гигиены
- Дано введение в структуру и этапы построения защищённой сети VipNet
- Рассмотрена примерная топология и IP-адресация для выполнения задания

---

**Следующий шаг:**  
Переход к практической части — разбор топологии и настройка компонентов VipNet.

## Часть 2
*Таймкод: 00:23:16.040 - 00:50:12.460*

# Video Transcript Summary: Corporate Network Setup & Subnetting (Chunk 2)

## Overview

This segment covers the practical setup of a corporate network simulation for an exam scenario, focusing on subnetting, IP addressing, and configuring virtual networks using ESXi. The instructor answers student questions, demonstrates subnet mask calculations, and begins the process of mapping virtual machines to network segments.

---

## Key Points & Concepts

### 1. Network Diagram and Subnet Assignment

- **Manual Network Diagramming**: The instructor demonstrates creating a network diagram by hand for clarity, mapping out the main office, branch office, and internet segments.
- **Subnet Assignments**:
  - Main office: e.g., 192.168.110.x
  - Branch office: e.g., 10.10.x.x
  - Internet: e.g., 198.18.10.x

#### Visual Illustration Recommended
- **[00:23:30]

![Скриншот в 00:23:30](./screenshots\screenshot_00-23-30.jpg)


![Скриншот в 00:23:30](./screenshots\screenshot_00-23-30.jpg)
**: Screenshot of the hand-drawn network diagram with labeled subnets.

---

### 2. Understanding "Координатор" (Coordinator)

- **Coordinator = Router**: The term "координатор" is essentially equivalent to a router, with some additional features specific to WebNet (encryption, custom commands).
- **Placement**: Coordinators (routers) are placed to filter both internal and external (internet) traffic, often using NAT for address translation.

---

### 3. Subnet Mask Conversion & Explanation

- **CIDR Notation**: Explanation of converting subnet masks from CIDR (e.g., /27) to dotted-decimal (e.g., 255.255.255.224).
- **Step-by-step Calculation**:
  - /27: 255.255.255.224
  - /26: 255.255.255.192
  - /28: 255.255.255.240
- **Binary Breakdown**: Demonstrates how to convert bits to decimal values for subnet masks.

#### Visual Illustration Recommended
- **[00:30:00]

![Скриншот в 00:30:00](./screenshots\screenshot_00-30-00.jpg)


![Скриншот в 00:30:00](./screenshots\screenshot_00-30-00.jpg)
**: Screenshot of the binary-to-decimal mask conversion in Word.

#### Example Calculation (as shown in transcript):
```plaintext
/27 mask in binary: 11111111.11111111.11111111.11100000
Decimal:           255.      255.      255.      224
```

---

### 4. Assigning IP Addresses

- **IP Assignment**: Specific IP addresses are assigned to each device in the network for clarity and future configuration.
  - Example:
    - Net1 database: 192.168.110.241
    - Coordinator: 192.168.110.242
    - Admin: 192.168.110.243
    - Operator: 192.168.110.244
    - Internet-facing: 198.18.10.1, 198.18.10.2
    - Branch: 10.10.10.194, 10.10.10.195

---

### 5. Exam & Documentation Requirements

- **Screenshots Required**: All key configuration steps must be documented with screenshots, saved in a dedicated folder (e.g., "Модуль 1") on the desktop.
- **Screenshot Naming Convention**: Use a standard format like ITCS1 for the first task.
- **Exam Duration**: Expected to be 4 hours.

---

### 6. Virtualization Environment

- **Platform**: ESXi will be used for the exam; for practice, VirtualBox is acceptable.
- **Pre-created VMs**: Six virtual machines will be provided, named according to their roles (e.g., Net1 admin, Net1 coordinator, Net1 database).
- **Database Node**: Net1 database is a special node for SQL installation and is not protected by WebNet client.

#### Visual Illustration Recommended
- **[00:46:00]

![Скриншот в 00:46:00](./screenshots\screenshot_00-46-00.jpg)


![Скриншот в 00:46:00](./screenshots\screenshot_00-46-00.jpg)
**: Screenshot of the ESXi interface showing the six VMs and their assigned roles.

---

### 7. ESXi Network Configuration

- **Virtual Switch & Port Groups**:
  - Create a virtual switch (e.g., "demo").
  - Create port groups for each network segment (office, branch, internet).
  - Assign each VM's network adapter to the appropriate port group.

#### Visual Illustration Recommended
- **[00:48:30]

![Скриншот в 00:48:30](./screenshots\screenshot_00-48-30.jpg)


![Скриншот в 00:48:30](./screenshots\screenshot_00-48-30.jpg)
**: Screenshot of ESXi's networking section with the virtual switch and port groups.

---

## Notable Q&A

- **Subnetting in Packet Tracer/GNS3**: Students can practice in Cisco Packet Tracer or GNS3, but the exam will use ESXi.
- **Location of WebNet Components**: Coordinators are placed at network boundaries to filter both internal and external traffic.
- **Virtualization Platform**: ESXi is mandatory for the exam, but practice can be done on any platform.

---

## Summary Table: Key Network Elements

| Segment        | Example Subnet         | Example Devices/Addresses           |
|----------------|-----------------------|-------------------------------------|
| Main Office    | 192.168.110.0/27      | .241 (DB), .242 (Coord), .243 (Admin), .244 (Oper) |
| Branch Office  | 10.10.10.0/26         | .194, .195                          |
| Internet       | 198.18.10.0/28        | .1, .2                              |

---

## Action Items for Students

- Practice subnet mask conversions and IP assignments.
- Prepare to document every configuration step with screenshots.
- Familiarize yourself with ESXi's interface, especially networking and VM settings.

---

## Timestamps for Key Visuals

- **[00:23:30]**: Initial network diagram with subnets
- **[00:30:00]**: Subnet mask binary-to-decimal conversion
- **[00:46:00]**: ESXi VM overview
- **[00:48:30]**: ESXi networking setup (virtual switch and port groups)

---

**End of Summary for Chunk 2**

## Часть 3
*Таймкод: 00:50:12.460 - 01:15:08.680*

# Video Transcript Summary: Network and SQL Server Setup

## Overview

This section of the video covers the configuration of virtual network adapters and the initial setup of a SQL Server database for a training or exam environment. The focus is on proper network segmentation, adapter assignment, and the installation and configuration of Microsoft SQL Server for use with a network management system.

---

## Key Points and Concepts

### 1. Virtual Network Configuration

- **Network Segmentation**: Separate networks are created for office, branch (филиал), and internet segments.
- **Adapter Assignment**:
  - Each virtual machine (VM) is assigned to the appropriate network.
  - Ensure the "Connect" checkbox is enabled for each adapter; otherwise, the VM will not be connected to the network.
- **Coordinator Setup**:
  - The coordinator VM requires four adapters, all enabled initially ([00:51:00]

![Скриншот в 00:51:00](./screenshots\screenshot_00-51-00.jpg)
).
  - Adapters are mapped as follows:
    - Adapter 0 (ES0): Internet-facing
    - Adapter 1 (ES1): Office or branch-facing
    - Adapters 2 and 3: Not used, will be disabled later
  - It’s crucial to document which adapter corresponds to which network to avoid confusion when assigning IP addresses.

#### **Visual Illustration Recommended**
- **Adapter assignment and network mapping diagram**  
  - Timestamp: [00:52:30]

![Скриншот в 00:52:30](./screenshots\screenshot_00-52-30.jpg)


![Скриншот в 00:52:30](./screenshots\screenshot_00-52-30.jpg)

- **Network settings screen showing adapters and "Connect" checkboxes**  
  - Timestamp: [00:53:10]

![Скриншот в 00:53:10](./screenshots\screenshot_00-53-10.jpg)


---

### 2. Virtual Machine Setup

- **Machines Configured**:
  - Coordinator(s)
  - Admin
  - Operator
  - Database server (net1 database)
  - Clients
- **Network Adapter Verification**:
  - Double-check that each VM is connected to the correct network segment.
  - Correction example: The net2 client should be connected to the branch, not the office ([01:01:00]

![Скриншот в 01:01:00](./screenshots\screenshot_01-01-00.jpg)


![Скриншот в 01:01:00](./screenshots\screenshot_01-01-00.jpg)
).

---

### 3. SQL Server Database Installation

- **Preparation**:
  - Attach the ISO image containing installation files (demo.so) to the VM ([01:03:00]

![Скриншот в 01:03:00](./screenshots\screenshot_01-03-00.jpg)


![Скриншот в 01:03:00](./screenshots\screenshot_01-03-00.jpg)
).
  - Copy SQL Server installer and Management Studio to the VM desktop.
- **Network Configuration**:
  - Assign static IP addresses according to the network plan.
  - Example for net1 database:  
    ```
    IP:      192.168.110.241
    Mask:    255.255.255.240
    Gateway: 192.168.110.242
    ```
  - Disable IPv6 to avoid conflicts.
  - Turn off Windows Firewall for the training environment ([01:07:30]

![Скриншот в 01:07:30](./screenshots\screenshot_01-07-30.jpg)


![Скриншот в 01:07:30](./screenshots\screenshot_01-07-30.jpg)
).
- **Time and Date**:
  - Set the system date to match the license validity (2024).
- **SQL Server Installation Steps**:
  - Choose "New SQL Server" installation.
  - Accept license terms.
  - Ignore update service connection errors.
  - Ensure all prerequisites are met (green checkmarks).
  - Disable "Air Services" during component selection.
  - Choose the correct database instance name: `WinNCC SQL` (for VIPNet).
  - Set SQL Server and SQL Server Browser to automatic startup.
  - Use "Mixed Mode" authentication (SQL + Windows), set the SA password ([01:11:00]

![Скриншот в 01:11:00](./screenshots\screenshot_01-11-00.jpg)


![Скриншот в 01:11:00](./screenshots\screenshot_01-11-00.jpg)


![Скриншот в 01:11:00](./screenshots\screenshot_01-11-00.jpg)
).
- **Documentation**:
  - Create a text file (`ip.txt`) on the desktop to record all IP addresses, logins, and passwords for each VM ([01:12:30]

![Скриншот в 01:12:30](./screenshots\screenshot_01-12-30.jpg)


![Скриншот в 01:12:30](./screenshots\screenshot_01-12-30.jpg)


![Скриншот в 01:12:30](./screenshots\screenshot_01-12-30.jpg)
).
  - Example entries:
    ```
    net1 database: 192.168.110.241
    net1 court c: 192.168.110.242
    admin c:      192.168.110.243
    oper c:       192.168.110.244
    ```

#### **Visual Illustration Recommended**
- **SQL Server installation wizard (Mixed Mode selection and SA password entry)**  
  - Timestamp: [01:11:00]
- **Example of the `ip.txt` file with documented addresses**  
  - Timestamp: [01:12:30]

---

### 4. Exam/Training Tips

- **Tasks on the Exam**:
  - The exam will likely follow similar steps: network setup, key issuance, and system verification.
  - Only minor changes (e.g., IP addresses, machine names) are expected year-to-year.
- **Best Practices**:
  - Document all configurations as you go to avoid mistakes.
  - Focus on understanding the workflow rather than memorizing exact values.

---

## Summary Table: Key Steps

| Step                       | Action/Setting                                         | Visual Ref.   |
|----------------------------|-------------------------------------------------------|---------------|
| Network Adapter Setup      | Assign and connect adapters per network segment        | [00:52:30]    |
| VM Network Verification    | Ensure correct adapter assignments                    | [01:01:00]    |
| ISO Attachment             | Mount demo.so ISO for software installation           | [01:03:00]    |
| IP Address Assignment      | Set static IPs, disable IPv6, set gateway             | [01:07:00]

![Скриншот в 01:07:00](./screenshots\screenshot_01-07-00.jpg)
    |
| Firewall                   | Disable for training purposes                         | [01:07:30]    |
| SQL Server Installation    | Mixed Mode, set SA password, use WinNCC SQL instance  | [01:11:00]    |
| Documentation              | Create ip.txt with all credentials and addresses      | [01:12:30]    |

---

## Notable Quotes

- *"Главное потом не запутаться и записать, что у вас где будет где нулевой, где первый."*
- *"Файл обязательный. И здесь вы должны все обязательно прописать."*

---

## Conclusion

This segment provides a step-by-step guide for setting up a virtualized network and preparing a SQL Server database for a network management system, emphasizing careful documentation and network configuration. The process is representative of what candidates can expect in the exam environment, with a focus on repeatable, logical steps.

## Часть 4
*Таймкод: 01:15:10.680 - 01:38:44.200*

# Video Transcript Summary: SQL Server Setup and Configuration for Network Management

## Overview

This section of the video covers the configuration of IP addresses, SQL Server installation and setup, the importance of documentation and screenshots during the exam, and initial steps for setting up the network management center. The focus is on preparing a reliable environment for further network management tasks and ensuring all steps are well-documented for assessment.

---

## Key Points

### 1. IP Address Assignment and User Setup

- **IP addresses** are assigned to network adapters and clients:
  - Example: `10.10.10.194` for one adapter, `10.10.195` for another client.
- **User accounts** are set up for each client, with corresponding IP addresses and passwords.
- All configuration details (IP addresses, passwords) should be recorded in a notepad or documentation file for reference.

### 2. SQL Server Installation

- **Mixed Mode** authentication is selected.
- **Administrator password** is set as per assignment requirements (e.g., `22XXxx`).
- **Install Only** option is chosen for SQL Server installation.
- SQL Server is installed independently and is **not directly tied to WIP Net**; it serves as a standalone database for configuration storage.

#### Visual Moment: SQL Server Installation Completion
- **Timestamp:** [01:19:30]

![Скриншот в 01:19:30](./screenshots\screenshot_01-19-30.jpg)


![Скриншот в 01:19:30](./screenshots\screenshot_01-19-30.jpg)

- *Screenshot recommended of the completed SQL Server installation window with all green checkmarks.*

### 3. Importance of Documentation and Screenshots

- **Screenshots are mandatory** at each key step to confirm task completion.
- Screenshots serve as evidence for examiners and can earn additional points.
- **Naming convention** for screenshots: `ITCS_<task number>_<screenshot number>`, with a descriptive caption.
- **First screenshot:** Database installation confirmation.
- **Second screenshot:** Database configuration confirmation.

#### Visual Moment: Screenshot Naming and Saving
- **Timestamp:** [01:22:15]

![Скриншот в 01:22:15](./screenshots\screenshot_01-22-15.jpg)


![Скриншот в 01:22:15](./screenshots\screenshot_01-22-15.jpg)

- *Screenshot of the file save dialog with the correct naming convention.*

### 4. SQL Server Configuration

- **SQL Server Services:** Ensure critical services are running:
  - `SQL Server`
  - `SQL Server Browser`
  - `SQL Server Reporter`
- **FileStream:** Enable FileStream and allow all clients to connect.
- **Network Protocols:** Enable required protocols in SQL Server Network Configuration:
  - `Shared Memory`
  - `Named Pipes`
  - `TCP/IP` (ensure the correct IP address is active and enabled)
- **Restart SQL Server** after changes.

#### Visual Moment: SQL Server Configuration Utility
- **Timestamp:** [01:26:40]

![Скриншот в 01:26:40](./screenshots\screenshot_01-26-40.jpg)


![Скриншот в 01:26:40](./screenshots\screenshot_01-26-40.jpg)

- *Screenshot of the SQL Server Configuration Manager with all necessary services and protocols enabled.*

### 5. Exam Tips and Workflow

- **Screenshots** at every major step protect against disputes and speed up the checking process.
- If a screenshot is missing, examiners may need to check the actual system, which is more time-consuming.
- **Documentation** should include all changes (IP addresses, passwords, configurations) in a dedicated file (e.g., `ip.txt`).

### 6. Transition to Network Management Center Setup

- **Next steps:** Install the network management center client (SUS) on the appropriate admin machine, not on the database server.
- **IP configuration** for the admin machine:
  - Example: `192.168.110.243` with subnet mask `255.255.255.240` and gateway `192.168.110.242`.
- **Tip:** Keep all IP addresses and configuration details handy on paper for quick reference during setup.

#### Visual Moment: Admin Machine IP Configuration
- **Timestamp:** [01:37:50]

![Скриншот в 01:37:50](./screenshots\screenshot_01-37-50.jpg)


![Скриншот в 01:37:50](./screenshots\screenshot_01-37-50.jpg)

- *Screenshot of the network adapter properties showing the correct IP, subnet mask, and gateway settings.*

---

## Summary Table

| Step                        | Key Action                                    | Screenshot? | Timestamp    |
|-----------------------------|-----------------------------------------------|-------------|--------------|
| SQL Server Installation     | Confirm install completion                    | Yes         | [01:19:30]   |
| Screenshot Naming           | Save screenshot with correct naming            | Yes         | [01:22:15]   |
| SQL Server Configuration    | Show services and protocols enabled           | Yes         | [01:26:40]   |
| Admin Machine IP Setup      | Show correct IP configuration                 | Yes         | [01:37:50]   |

---

## Recommendations

- **Always document** every configuration step and change.
- **Take screenshots** at every critical milestone, especially for installations and service configurations.
- **Follow naming conventions** for all files and screenshots to ensure easy verification.
- **Keep configuration details accessible** to streamline setup and avoid errors.

---

**End of Summary for Chunk 4**

## Часть 5
*Таймкод: 01:38:44.200 - 02:06:12.420*

# Видеоразбор: Установка и настройка Webnet Администратора и связанных компонентов

## Основные этапы и ключевые моменты

### 1. Проверка сетевых настроек и связи с базой данных

- Важно, чтобы время на всех машинах в сети совпадало, особенно с машиной администратора.
- Проверка сетевых параметров: IP-адрес, шлюз, маска.
- Отключение брандмауэра для корректной работы.
- Проверка связи с SQL сервером через команду `ping`.
    - В отчёте рекомендуется зафиксировать наличие связи с базой данных (скриншот не обязателен, но желателен для спорных моментов).
    - **Важный момент для скриншота:** успешный пинг до SQL сервера [01:39:30]

![Скриншот в 01:39:30](./screenshots\screenshot_01-39-30.jpg)


![Скриншот в 01:39:30](./screenshots\screenshot_01-39-30.jpg)


### 2. Подключение образа демо и подготовка ПО

- Подключение ISO-образа демо через CD/DVD-привод виртуальной машины.
- Проверка, что ISO-образ корректно подключён (Connect/Power On).
- Подготовка необходимых программ:
    - AnyToISO (для работы с ключами в формате ISO)
    - Webnet Администратор
    - Webnet Клиент
    - CA-Informing

### 3. Структура и последовательность установки Webnet Администратора

- **Webnet Администратор** состоит из:
    - Центр управления сетью (ЦУС)
        - Серверная часть
        - Клиентская часть
    - Ключевой центр (КЦ)
- **Обязательная последовательность установки:**
    1. Центр управления сетью (сервер)
    2. Центр управления сетью (клиент)
    3. Ключевой центр

### 4. Установка Центра управления сетью (сервер)

- Запуск установки, выбор языка, принятие соглашения.
- Важно: при указании имени сервера указывается IP-адрес SQL сервера, а не "точка" (локальный сервер).
- Проверка подлинности через SQL (mixed mode), ввод логина SA и пароля.
- Возможная ошибка при подключении к базе данных (ошибка с FileStream).

    - **Важный момент для скриншота:** появление ошибки подключения к SQL серверу [01:52:30]

![Скриншот в 01:52:30](./screenshots\screenshot_01-52-30.jpg)


![Скриншот в 01:52:30](./screenshots\screenshot_01-52-30.jpg)


### 5. Исправление ошибки FileStream в SQL Server

- Запуск SQL Server Management Studio (SSMS).
- Подключение к базе данных, переход в свойства базы.
- Вкладка "Advanced" → параметр "FileStream" переводится в "Full access enabled".
- Перезапуск SQL сервера через конфигуратор.
- Повторная попытка установки — ошибка должна исчезнуть.

    - **Важный момент для скриншота:** изменение параметра FileStream в SSMS [01:59:00]

![Скриншот в 01:59:00](./screenshots\screenshot_01-59-00.jpg)


![Скриншот в 01:59:00](./screenshots\screenshot_01-59-00.jpg)

    - **Важный момент для скриншота:** успешная проверка подключения после исправления [02:01:00]

![Скриншот в 02:01:00](./screenshots\screenshot_02-01-00.jpg)


![Скриншот в 02:01:00](./screenshots\screenshot_02-01-00.jpg)


### 6. Дальнейшая установка компонентов

- Установка клиента Центра управления сетью.
    - После установки появляется соответствующий значок.
- Установка Ключевого центра.
- Установка CA-Informing.
- Установка Webnet клиента (для соединения между машинами).

    - **Важный момент для скриншота:** итоговый список установленных программ [02:05:30]

![Скриншот в 02:05:30](./screenshots\screenshot_02-05-30.jpg)


![Скриншот в 02:05:30](./screenshots\screenshot_02-05-30.jpg)


### 7. Организационные моменты по стендам и экзамену

- В период подготовки количество стендов ограничено (примерно по 8 на группу), возможна работа в группах.
- На самом экзамене у каждого будет свой стенд.
- Даты экзамена: начало с 1-2 июня, распределение по потокам.
- Стенды будут работать круглосуточно.

---

## Важные визуальные моменты (скриншоты)

- [01:39:30] — Успешный пинг до SQL сервера (доказательство связи)
- [01:52:30] — Ошибка подключения к SQL серверу (FileStream)
- [01:59:00] — Изменение FileStream в SSMS (Advanced → Full access enabled)
- [02:01:00] — Успешная проверка подключения после исправления
- [02:05:30] — Итоговый список установленных программ (для отчёта)

---

## Технические детали (пример заполнения параметров при установке сервера)

```plaintext
Имя сервера: <IP-адрес SQL сервера, например 192.168.110.241>
Проверка подлинности: SQL Server Authentication
Пользователь: SA
Пароль: <ваш_пароль>
```

---

## Итоги

- Проведена полная установка и настройка Webnet Администратора с необходимыми компонентами.
- Описаны типовые ошибки и способы их устранения.
- Даны рекомендации по фиксации ключевых этапов с помощью скриншотов для отчёта.
- Рассмотрены организационные вопросы по работе со стендами и экзамену.

**Рекомендация:** Делайте скриншоты на каждом ключевом этапе для отчётности и решения спорных вопросов.

## Часть 6
*Таймкод: 02:06:12.420 - 02:34:40.060*

# Summary of Transcript Chunk 6 (02:06:12.420 – 02:34:40.060)

## Overview

This section covers the step-by-step process of installing and configuring various components for a secure network environment, focusing on the setup of clients and coordinators (servers), network configuration, and initial network structure creation using the VipNet system. The instructions are practical, with emphasis on making and saving screenshots at each critical step for documentation and exam purposes.

---

## Key Points & Steps

### 1. Task Structure and Preparation
- There are **5 main tasks** to complete in this section.
- Most time is spent on **installing software** on different machines.
- **Screenshots** are required at each significant step for documentation.

---

### 2. Installation of VipNet Client for Linux (RedOS)
- The process involves mounting the installation ISO and running the installer.
- **Password entry** is required during installation.
- After installation:
  - The client is moved to the desktop for easy access.
  - **Security warnings** may appear and can be ignored.
- **Screenshot required:** After successful installation and first launch.
  - **Timestamp:** [02:09:00]

![Скриншот в 02:09:00](./screenshots\screenshot_02-09-00.jpg)


![Скриншот в 02:09:00](./screenshots\screenshot_02-09-00.jpg)
 (approximate, after installation and first launch)

---

### 3. Installation on Windows Clients
- Similar steps are followed for Windows-based clients:
  - Install the VipNet client.
  - Adjust system date/time if using an old license.
  - Disable firewall (Bradmower) for testing.
  - Configure network settings (IP address, subnet mask, gateway).
- **Important:** Each step, especially installation and first launch, must be documented with screenshots.
  - **Screenshot required:** Installation process, directory where software is installed, and first launch.
  - **Timestamp:** [02:19:00]

![Скриншот в 02:19:00](./screenshots\screenshot_02-19-00.jpg)


![Скриншот в 02:19:00](./screenshots\screenshot_02-19-00.jpg)
 (approximate, after installation and directory screenshot)

---

### 4. Network Configuration
- **Manual network settings** are configured for both Linux and Windows clients:
  - Assign static IP addresses.
  - Set subnet masks and gateways according to the network plan.
  - Verify connectivity with `ping` and `ip a` commands.
- **Screenshot required:** Network settings and successful connectivity test.
  - **Timestamp:** [02:23:00]

![Скриншот в 02:23:00](./screenshots\screenshot_02-23-00.jpg)


![Скриншот в 02:23:00](./screenshots\screenshot_02-23-00.jpg)
 (approximate, after network configuration)

---

### 5. Documentation and Exam Requirements
- For the exam, **every step must be documented with screenshots**:
  - Installation process
  - Directory of installed software
  - First launch of the application
- **Naming conventions** for screenshots are specified (e.g., "first launch", "directory", etc.).

---

### 6. Setting Up the Network Structure in VipNet Administrator

#### Accessing the Network Management Center
- Log in to the **VipNet Network Management Center** (ЦУС) as "Administrator".
- Default credentials: `Administrator` (first letter uppercase, in English).
- **Password management:** Change and document the new password in a text file for future reference.
- **Screenshot required:** Login screen and password change process.
  - **Timestamp:** [02:27:00]

![Скриншот в 02:27:00](./screenshots\screenshot_02-27-00.jpg)


![Скриншот в 02:27:00](./screenshots\screenshot_02-27-00.jpg)
 (approximate, during login and password setup)

#### Creating the Network Structure
- Choose to **manually configure the network structure** (do not use the automatic wizard).
- Add roles and nodes according to the assignment:
  - **Coordinators:** Add two (CA and SUB), each with the correct role (e.g., VA 1000).
  - **Clients:** Add three clients (adminca, user1, user2), each linked to the appropriate coordinator.
    - `adminca` is marked as the main administrator (flagged).
    - `user1` is linked to the office coordinator (CA).
    - `user2` is linked to the filial coordinator (SUB).
- **Screenshot required:** Network structure diagram and roles assignment.
  - **Timestamp:** [02:31:00]

![Скриншот в 02:31:00](./screenshots\screenshot_02-31-00.jpg)


![Скриншот в 02:31:00](./screenshots\screenshot_02-31-00.jpg)
 (approximate, after network structure setup)

#### Additional Notes
- The **database node** is not included in the main network structure.
- The system displays the number of coordinators, clients, and users, which should be cross-checked with the assignment.

---

## Visual Illustration Recommendations

| Step                                 | What to Capture                  | Timestamp   |
|---------------------------------------|----------------------------------|-------------|
| VipNet Client for Linux Installed     | App on desktop, first launch     | [02:09:00]  |
| Windows Client Installation           | Install process, directory, run  | [02:19:00]  |
| Network Configuration                 | Network settings, ping results   | [02:23:00]  |
| VipNet Admin Login & Password Change  | Login screen, password change    | [02:27:00]  |
| Network Structure in VipNet Admin     | Diagram, roles assignment        | [02:31:00]  |

---

## Technical Content

### Example: Static IP Configuration (Linux)
```bash
# Set static IP for Linux client
sudo nano /etc/network/interfaces
# Add:
auto eth0
iface eth0 inet static
    address 192.168.110.244
    netmask 255.255.255.240
    gateway 192.168.110.242
```

---

## Important Reminders

- **Screenshots at every step** are crucial for exam documentation.
- **Naming and saving** screenshots as per instructions is required.
- **Manual configuration** is preferred over automatic wizards for full control and to match exam expectations.
- **Password and network details** must be carefully documented and stored.

---

## Summary

This chunk provides a comprehensive walkthrough for installing and configuring VipNet clients and coordinators on both Linux and Windows, setting up the network structure, and documenting every step with screenshots for exam purposes. The process emphasizes manual configuration, careful documentation, and adherence to assignment requirements.

## Часть 7
*Таймкод: 02:34:40.060 - 02:58:01.220*

# Summary of Transcript Chunk 7 (02:34:40.060 – 02:58:01.220)

## Overview

This segment covers the finalization of a secure network setup, including:
- Assigning user roles and configuring user communication permissions
- Verifying network structure and exporting configuration reports
- Generating and distributing cryptographic keys
- Preparing key containers and ISO images for deployment

---

## 1. Assigning Roles to Users

- **Network Structure**: 3 clients and 2 coordinators are established.
- **Role Assignment**:
  - For main users, roles such as `network control center`, `business mail`, and `VPN client` are added.
  - Linux client receives only one role due to system limitations.
  - Windows client receives `business VPN` and messaging/file exchange roles.
- **Key Visual Step**: Adding roles to users and confirming assignments  
  **Timestamp**: [02:35:00]

![Скриншот в 02:35:00](./screenshots\screenshot_02-35-00.jpg)


![Скриншот в 02:35:00](./screenshots\screenshot_02-35-00.jpg)


---

## 2. Configuring User Communication

- **Communication Matrix**: A table defines which users can communicate with each other (marked with checkmarks or asterisks).
- **Configuration Steps**:
  - For each user, the allowed communication links are set up in the user properties under "User Connections".
  - Verification is done by cross-referencing the table and user properties.
- **Key Visual Step**: Setting up and verifying user communication links  
  **Timestamp**: [02:37:00]

![Скриншот в 02:37:00](./screenshots\screenshot_02-37-00.jpg)


![Скриншот в 02:37:00](./screenshots\screenshot_02-37-00.jpg)


---

## 3. Documenting Network Structure

- **Screenshots**: Recommended to take screenshots of:
  - Coordinators
  - Clients
  - All users and their roles/permissions
- **Best Practice**: Screenshot each user node for documentation and verification.
- **Key Visual Step**: Taking screenshots of network structure and user roles  
  **Timestamp**: [02:41:00]

![Скриншот в 02:41:00](./screenshots\screenshot_02-41-00.jpg)


![Скриншот в 02:41:00](./screenshots\screenshot_02-41-00.jpg)


---

## 4. Verifying and Exporting Network Configuration

- **Network Validation**:
  - Use the "Check network configuration" feature to ensure no errors or incomplete data.
  - If errors are found (e.g., missing roles), the system highlights them for correction.
- **Report Export**:
  - Export the network structure report in HTML format as required by the assignment.
  - Save all related files to a designated folder on the desktop for easy access.
- **Key Visual Step**: Running network validation and exporting HTML report  
  **Timestamp**: [02:45:00]

![Скриншот в 02:45:00](./screenshots\screenshot_02-45-00.jpg)


![Скриншот в 02:45:00](./screenshots\screenshot_02-45-00.jpg)


---

## 5. Generating and Managing Cryptographic Keys

- **Key Generation Workflow**:
  - Launch the Key Center and create a new database.
  - Enter the SQL server IP address and default settings.
  - Set and record the administrator password (store in a text file for reference).
  - Remove the auto-lock setting (uncheck the 15-minute auto mode).
  - Use a password (not a passphrase) for key protection.
- **Key Visual Step**: Key Center setup and password assignment  
  **Timestamp**: [02:51:00]

![Скриншот в 02:51:00](./screenshots\screenshot_02-51-00.jpg)


![Скриншот в 02:51:00](./screenshots\screenshot_02-51-00.jpg)


- **Creating Key Containers**:
  - For each network node, generate a key container.
  - Assign user and administrator passwords for each container (same password for all users for simplicity).
  - Store all passwords in a text file for later use.
- **Key Visual Step**: Creating and assigning passwords to key containers  
  **Timestamp**: [02:53:00]

![Скриншот в 02:53:00](./screenshots\screenshot_02-53-00.jpg)


![Скриншот в 02:53:00](./screenshots\screenshot_02-53-00.jpg)


---

## 6. Preparing Key Distribution

- **Organizing Keys**:
  - Move all generated key files into a designated subfolder (e.g., "задание 1.6").
  - Avoid simply dragging files without proper organization, as this can cause client issues.
- **Creating ISO Image**:
  - Use an ISO creation tool to package the key folder for deployment, especially for Linux clients.
  - Rename the ISO file using Latin characters to avoid compatibility issues.
- **Key Visual Step**: Creating ISO image from key folder  
  **Timestamp**: [02:55:00]

![Скриншот в 02:55:00](./screenshots\screenshot_02-55-00.jpg)


![Скриншот в 02:55:00](./screenshots\screenshot_02-55-00.jpg)


---

## 7. Final Steps and Best Practices

- **Status Monitoring**:
  - Always check the status in the Key Center to ensure the correct workflow (e.g., "awaiting keys").
  - After distributing keys, set administrator passwords for coordinators.
- **Documentation**:
  - Keep a detailed text file with all passwords and roles for reference and troubleshooting.
- **Key Visual Step**: Setting administrator passwords for coordinators  
  **Timestamp**: [02:57:00]

![Скриншот в 02:57:00](./screenshots\screenshot_02-57-00.jpg)


![Скриншот в 02:57:00](./screenshots\screenshot_02-57-00.jpg)


---

## Notable Best Practices

- Always verify network configuration before exporting or distributing keys.
- Document every password and role assignment.
- Use screenshots to capture the state of the network and user permissions for reporting and verification.

---

## Technical Snippet Example

```plaintext
IP Address for SQL Server: 192.168.110.241
Admin Password (example): 2111xx
Key File Format: .DST
ISO Image Name: keys.iso
```

---

## Visual Illustration Recommendations

- **[02:35:00]**: User role assignment dialog
- **[02:37:00]**: User communication matrix and connection setup
- **[02:41:00]**: Screenshot of all user nodes and roles
- **[02:45:00]**: Network validation and HTML report export screen
- **[02:51:00]**: Key Center setup and password entry
- **[02:53:00]**: Key container creation and password assignment
- **[02:55:00]**: ISO image creation process
- **[02:57:00]**: Setting administrator passwords for coordinators

---

This summary captures the essential steps and best practices for finalizing a secure network setup, documenting configurations, and preparing cryptographic materials for deployment.

## Часть 8
*Таймкод: 02:58:01.220 - 03:26:19.760*

# Video Transcript Summary: Key Management and Network Configuration

## Overview

This section of the video covers the process of setting up and distributing cryptographic keys within a network environment, configuring user groups, and troubleshooting common issues—especially when working with both Windows and Linux clients in a virtualized infrastructure (using ESXi). The workflow emphasizes the importance of proper password management, group creation, and key distribution, with attention to platform-specific nuances.

---

## Key Points and Concepts

### Password and Key Management

- **Unique Passwords:** Each user and coordinator must have a unique password as per assignment requirements.
- **Documentation:** All steps, especially password assignments and key distributions, should be documented with screenshots for verification purposes.  
  *Visual Moment: Assigning passwords to users and coordinators* [03:00:00]

![Скриншот в 03:00:00](./screenshots\screenshot_03-00-00.jpg)


![Скриншот в 03:00:00](./screenshots\screenshot_03-00-00.jpg)


### Key Distribution Process

- **Key Transfer to Central Management:** Keys are created and transferred to the central key management system (ЦУС).
- **Status Tracking:** The status of key distribution is monitored ("Передан в СУС", "Готова к отправке").
- **Group Creation:** Node groups for "Office" and "Branch" are created and populated with relevant users and coordinators.
  *Visual Moment: Creating and naming node groups* [03:05:00]

![Скриншот в 03:05:00](./screenshots\screenshot_03-05-00.jpg)


![Скриншот в 03:05:00](./screenshots\screenshot_03-05-00.jpg)


### Assigning Users to Groups

- **User Assignment:** Users and devices are added to their respective groups (Office: admin, coordinator, user1; Branch: coordinator, user).
- **Group Administrator Passwords:** Each group receives an administrator password, also documented.
  *Visual Moment: Assigning users to groups and setting group admin passwords* [03:08:00]

![Скриншот в 03:08:00](./screenshots\screenshot_03-08-00.jpg)


![Скриншот в 03:08:00](./screenshots\screenshot_03-08-00.jpg)


### Key Installation on Clients

- **Windows Client:** Keys are installed via the Vitnet client; password entry is required for activation.
- **Linux Client:** Key installation is more complex, requiring additional network configuration.
  *Visual Moment: Installing keys on Windows and Linux clients* [03:12:00]

![Скриншот в 03:12:00](./screenshots\screenshot_03-12-00.jpg)


![Скриншот в 03:12:00](./screenshots\screenshot_03-12-00.jpg)


### File Transfer via ESXi

- **Datastore Usage:** Key files are uploaded to the ESXi datastore for distribution to virtual machines.
- **Network Adapter Configuration:** Temporary changes to VM network adapters are made to facilitate file transfer, then reverted.
  *Visual Moment: Uploading key files to ESXi datastore* [03:15:00]

![Скриншот в 03:15:00](./screenshots\screenshot_03-15-00.jpg)


![Скриншот в 03:15:00](./screenshots\screenshot_03-15-00.jpg)


### Troubleshooting and Platform-Specific Issues

- **Linux-Specific Configuration:** Linux clients require explicit configuration of external network addresses for coordinators, unlike Windows.
- **Error Handling:** If errors occur (e.g., key distribution failures), restarting the management center or re-uploading keys often resolves the issue.
  *Visual Moment: Adding external network addresses for coordinators* [03:20:00]

![Скриншот в 03:20:00](./screenshots\screenshot_03-20-00.jpg)


![Скриншот в 03:20:00](./screenshots\screenshot_03-20-00.jpg)


### Regenerating and Redistributing Keys

- **Key Updates:** When network settings change, new keys must be generated and distributed to affected clients.
- **File Management:** Old key files can remain in the datastore; only correct keys should be installed on clients.

### Final Steps and Verification

- **Key Activation:** After updating and distributing keys, clients are prompted for passwords to activate new keys.
- **Network Permissions:** When prompted by the system, always allow network access for the client application to ensure connectivity.
  *Visual Moment: Allowing network access prompt* [03:25:00]

![Скриншот в 03:25:00](./screenshots\screenshot_03-25-00.jpg)


![Скриншот в 03:25:00](./screenshots\screenshot_03-25-00.jpg)


---

## Notable Visual Moments

| Description                                                      | Timestamp   |
|------------------------------------------------------------------|-------------|
| Assigning passwords to users and coordinators                     | [03:00:00]  |
| Creating and naming node groups                                   | [03:05:00]  |
| Assigning users to groups and setting group admin passwords       | [03:08:00]  |
| Installing keys on Windows and Linux clients                      | [03:12:00]  |
| Uploading key files to ESXi datastore                            | [03:15:00]  |
| Adding external network addresses for coordinators (Linux)        | [03:20:00]  |
| Allowing network access prompt on client                          | [03:25:00]  |

---

## Technical Notes

```plaintext
- Always use unique passwords for each user and group administrator.
- For Linux clients, ensure all relevant external IP addresses are configured for coordinators.
- When transferring files via ESXi:
    1. Change VM network adapter to access the required network.
    2. Upload key files to the datastore.
    3. Revert network adapter settings after transfer.
- If key distribution fails, restart the management center and retry.
```

---

## Tips and Best Practices

- **Screenshot Documentation:** Take screenshots at every critical step for assignment verification.
- **File Organization:** Clearly name key files and group folders to avoid confusion during distribution.
- **Error Awareness:** Be prepared to handle platform-specific issues, especially with Linux clients.
- **Network Settings:** Always double-check network adapter configurations before and after file transfers.

---

This summary captures the essential workflow and troubleshooting steps for secure key management and network configuration in a mixed OS virtual environment.

## Часть 9
*Таймкод: 03:26:19.760 - 03:50:16.160*

# Summary of Transcript Chunk 9 (03:26:19.760 – 03:50:16.160)

## Key Steps in Key Distribution and Initial Setup

- **Key Distribution**
  - Keys are distributed to two coordinators and User2.
  - ISO files are used for key transfer; ensure "Connect" is checked during the process.
  - After installation, verify all clients have received their keys.
  - *Visual checkpoint*: Take screenshots of key installation for all clients.  
    **Timestamp:** [03:27:00]

![Скриншот в 03:27:00](./screenshots\screenshot_03-27-00.jpg)


![Скриншот в 03:27:00](./screenshots\screenshot_03-27-00.jpg)


- **Launching and Configuring VIPNet Client**
  - User2's key is installed via the VIPNet client.
  - Successful installation is confirmed by a notification.
  - *Visual checkpoint*: Screenshot showing successful key installation.  
    **Timestamp:** [03:28:00]

![Скриншот в 03:28:00](./screenshots\screenshot_03-28-00.jpg)


![Скриншот в 03:28:00](./screenshots\screenshot_03-28-00.jpg)


- **Initial Coordinator Setup**
  - Demonstrates the initial setup for the first coordinator; the second is similar.
  - Use the second installation mode (with GUI) for easier configuration.
  - Accept license, select region (Europe, Russia, Moscow), and set the year to match the license (2024).
  - Choose the CD option to load keys.
  - Enter the password created during key transfer.
  - *Visual checkpoint*: Screenshot of region and year selection during setup.  
    **Timestamp:** [03:32:00]

![Скриншот в 03:32:00](./screenshots\screenshot_03-32-00.jpg)


![Скриншот в 03:32:00](./screenshots\screenshot_03-32-00.jpg)


- **Network Configuration**
  - Assign static IP addresses for each network interface (e.g., 198.17.10.1 for the ground floor).
  - Clearly document which IP corresponds to which "floor" (ES 0 = ground, ES 1 = first, etc.) to avoid confusion.
  - Disable unused network interfaces (set to "down").
  - Set gateway, custom DNS (e.g., 8.8.8.8), and activate INCPE Server.
  - Assign the hostname as a single word (no spaces or dots), e.g., "coordinatorCA".
  - *Visual checkpoint*: Screenshot of interface configuration and hostname assignment.  
    **Timestamp:** [03:37:00]

![Скриншот в 03:37:00](./screenshots\screenshot_03-37-00.jpg)


![Скриншот в 03:37:00](./screenshots\screenshot_03-37-00.jpg)


- **Finalizing Setup**
  - Do not enable VPN with host during setup.
  - Complete the configuration; the coordinator is now set up.
  - The process for the second coordinator is the same, except the gateway points to the first coordinator.

## Exam and Module 1 Guidance

- **Module 1 is the Primary Focus**
  - On the demo exam, Module 1 is the main part to complete; most students do not reach Module 2 due to time constraints.
  - All tasks completed in this walkthrough are expected for Module 1.
  - Scoring: 100 points are allocated to Module 1 if only it is completed; points are doubled if both modules are done, but this rarely happens.
  - *Visual checkpoint*: Screenshot of the VIPNet client showing all connections/monitors lit up for all users and coordinators.  
    **Timestamp:** [03:44:00]

![Скриншот в 03:44:00](./screenshots\screenshot_03-44-00.jpg)


![Скриншот в 03:44:00](./screenshots\screenshot_03-44-00.jpg)


- **Important Exam Tips**
  - Always take screenshots of key steps, especially user connections in VIPNet client and network configuration.
  - Screenshots can be combined for efficiency if they clearly show all required information.
  - Be meticulous with digital hygiene (e.g., locking screens, pushing in chairs) to avoid losing points.

## Troubleshooting and Practical Advice

- **Common Issues**
  - VIPNet can be buggy; restarting the application often resolves issues.
  - If connections or keys are missing, recheck configuration and reapply keys if necessary.
  - *Visual checkpoint*: Screenshot of user connections in the network management center.  
    **Timestamp:** [03:46:00]

![Скриншот в 03:46:00](./screenshots\screenshot_03-46-00.jpg)


![Скриншот в 03:46:00](./screenshots\screenshot_03-46-00.jpg)


- **Resource Requirements**
  - Example setup: Each VM can run with 2–4 GB RAM and 1–2 CPUs, but more resources improve performance.
  - It is possible to set up the environment at home using VirtualBox, but the exam will use ESXi.
  - Distributives and images (including the coordinator) can be shared via Yandex Disk.

## Q&A Highlights

- **Combining Screenshots**
  - Allowed if all required information is visible and clear for the examiner.

- **Resource Sharing**
  - Images and coordinator distributives will be uploaded for student access.

- **Performance Considerations**
  - Lower resources will slow down VMs but are workable for practice.

---

## Visual Illustration Recommendations

- **[03:27:00]**: Screenshot of key installation process for coordinators and User2.
- **[03:28:00]**: Confirmation dialog of successful key installation in VIPNet client.
- **[03:32:00]**: Region and year selection screen during coordinator setup.
- **[03:37:00]**: Network interface configuration and hostname assignment.
- **[03:44:00]**: VIPNet client showing all monitors/connections active.
- **[03:46:00]**: Network management center displaying all user connections.

---

## Technical Configuration Example

```plaintext
# Example Static IP Assignment
Ground Floor (ES 0): 198.17.10.1
First Floor (ES 1): 192.168.110.242
Subnet Mask: 255.255.240.0
Gateway: 198.18.10.2
DNS: 8.8.8.8
Hostname: coordinatorCA (no spaces/dots)
```

---

**Note:** Careful documentation, clear screenshots, and attention to detail in configuration are critical for successful completion and full scoring on the exam.

## Часть 10
*Таймкод: 03:50:16.160 - 03:53:56.980*

# Video Transcript Summary: Demo Folder Organization & Session Wrap-Up

## Key Points

- **Demo Folder Organization**
  - Participants are reminded to keep demo folders organized and not clutter the workspace with unnecessary files.
  - *Passwords should not be left in visible places*; if stored, they should be inside folders and not openly accessible.
  - The organization of files and folders is important for maintaining a clean working environment, especially on shared or virtual desktops.

- **Virtual Machines Clarification**
  - The discussed hygiene practices (such as folder organization) apply to local desktops rather than virtual machines.

- **End of Session Instructions**
  - If there are any questions, participants are encouraged to reach out for clarification.
  - The session is wrapping up, and participants are told they can disconnect if there are no further questions.

- **Access to Demo Stands**
  - Access credentials for demo stands will likely be distributed the next day ([03:52:00]

![Скриншот в 03:52:00](./screenshots\screenshot_03-52-00.jpg)


![Скриншот в 03:52:00](./screenshots\screenshot_03-52-00.jpg)
).
  - Participants are encouraged to set up locally if possible for better performance, as network access may be slower.

- **Group Coordination**
  - Distribution of access may be coordinated through group leaders or curators.

- **Recording Availability**
  - The session recording will be available on RuTube ([03:53:20]

![Скриншот в 03:53:20](./screenshots\screenshot_03-53-20.jpg)


![Скриншот в 03:53:20](./screenshots\screenshot_03-53-20.jpg)
).

- **Session Conclusion**
  - The instructor thanks everyone and wishes them success with their demo submissions.
  - Multiple participants express their thanks and say goodbye.

## Notable Visual Moments

- **Distribution of Demo Stand Access**  
  *Visual: Screenshot of the announcement or list of demo stand access credentials being distributed.*  
  **Timestamp:** [03:52:00]

- **Recording Location Announcement**  
  *Visual: Screenshot showing the RuTube page or link where the recording will be available.*  
  **Timestamp:** [03:53:20]

---

**Summary:**  
This final session segment emphasizes the importance of workspace hygiene, particularly regarding folder organization and password security. It provides logistical details about upcoming demo stand access, encourages local setup for better performance, and informs participants about where to find the session recording. The session concludes with well-wishes and participant farewells.


---
*Конец документа*