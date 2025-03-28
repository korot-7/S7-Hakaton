# 🚀 Техническое решение

## 📌 Третий этап: Технические артефакты

### 🏗️ Описание архитектуры решения

📍 Диаграмма, описывающая решение: 🔗 [Ссылка на диаграмму](https://miro.com/app/board/uXjVINBMoSM=/)

🛠️ Используемые технологии и языки

☕ Java: Spring Boot, TelegramBots API, стандартные утилиты Java

🐍 Python: OpenCV (cv2), Caffe – фреймворк для глубинного обучения, json, requests, time

### 📷 Как работает решение?

1️⃣ Получаем изображения с камер с помощью OpenCV

2️⃣ Обрабатываем их при помощи нейросетевой модели

3️⃣ Определяем количество людей и отправляем данные в JSON-формате на сервер

4️⃣ Данные передаются в Telegram-бота, который уведомляет пользователей о загруженности


### 🤖 Модель машинного обучения

🔍 Мы используем MobileNet, экспортированную в формате Caffe:

📝 deploy.prototxt – текстовый файл, описывающий архитектуру сети

📂 mobilenet_iter_73000.caffemodel – файл с обученными весами

⚡ Модель загружается с помощью OpenCV и используется для обнаружения людей на видео

### 🔮 Перспективы масштабирования

### 💡 Будущие функции:

✅ Уведомления при высокой загруженности стойки

✅ Поддержка нескольких камер для более точного анализа

✅ Статистика загруженности за период

✅ Прогнозирование загруженности с помощью машинного обучения

✅ Отслеживание не только стоек регистрации, но и выходов на посадку

### 📈 Развитие продукта:
📱 Создание мобильного приложения с расширенным функционалом

✈️ Масштабирование системы на все аэропорты S7

🌍 Добавление поддержки нескольких языков


### ⚙️ Инструкция по развертыванию

📌 Ссылка на репозиторий с кодом: 💻 [Исходный код](https://github.com/miroslav0221/TG-Bot-S7-Hakaton/tree/1d7fce32c9fd4ab0d464a55708ec9a7fa81408af)


🔧 Порядок запуска:

1️⃣ Запустить сервер: ServerApplication.java (директория server)

2️⃣ Запустить обработку изображений: send_information.py (директория OpenCV)

3️⃣ Запустить Telegram-бота: BotApplication.java (директория bot)

📌 Важно:

Все устройства должны быть в одной локальной сети с разрешенным взаимодействием.

В файле send_information.py укажите корректные URL-адреса видеопотоков (можно использовать мобильные приложения, например, "IP Webcam" для Android).

🖼️ Примеры настройки URL-адресов:

<p align="center"> <img width="600px" src="photo_from_phone_with_URL-address.png" alt="photo_from_phone_with_URL-address.png"/> </p> <p align="center"> <img width="600px" src="screen_from_code_with_URL-address.png" alt="screen_from_code_with_URL-address.png"/> </p>
📍 Адрес с первого фото необходимо вставить в соответствующее поле словаря camera_indices (см. второе фото).

### 🎥 Демо-стенд

📽️ Видео с примером работы нашего продукта:

▶️ Перейти к видео

[Видео с примером работы нашего продукта](https://drive.google.com/drive/folders/1o_33bFJ_r3n6CBTdfLVz46VMpoeMndsr?usp=sharing)
