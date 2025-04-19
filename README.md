📝 Django Blog Project(Grim)
Полноценный блог на Django с поддержкой регистрации пользователей, редактирования профиля, аватаров и CRUD-функциональностью для постов.
📌 О проекте
Этот блог — это не просто учебный шаблон, а настоящая база для запуска собственного онлайн-продукта. Он построен с учётом расширяемости и лёгкости интеграции с другими сервисами — будь то веб-интерфейс, мобильное приложение, или даже Telegram-бот.

Проект идеально подходит:
Для персонального блога или портфолио
Для блога небольшой компании или стартапа
Как CMS-ядро для Telegram-бота (например, бот, публикующий посты или уведомления)
Для тестирования интеграции Django с внешними API
Как стартовая точка для изучения Django + пользователей + медиа
Архитектура проекта разделена по приложениям (blog, users), что делает код масштабируемым, понятным и готовым к рефакторингу или автоматизации.

📌 Особенности проекта
Регистрация, вход и выход пользователей
Профиль с возможностью загрузки аватара
Создание, редактирование и удаление постов
Просмотр всех постов и постов отдельного пользователя
Чистый, адаптивный интерфейс на Bootstrap

Категория | Технологии
Язык | Python 3
Фреймворк | Django
UI | HTML, CSS, Bootstrap 4,5
Формы | Django Crispy Forms
Работа с медиа | Pillow
База данных | SQLite (по умолчанию)

🚀 Установка и запуск
1. Клонирование репозитория
git clone https://github.com/yourusername/django-blog.git
cd django-blog

2. Установка зависимостей
Создайте виртуальное окружение и активируйте его:
python -m venv venv
source venv/bin/activate  # для Linux/macOS
venv\Scripts\activate     # для Windows

Установите зависимости:
pip install -r requirements.txt

3. Примените миграции и создайте суперпользователя
python manage.py migrate
python manage.py createsuperuser

4. Запуск проекта
python manage.py runserver

Теперь проект доступен по адресу: http://127.0.0.1:8000

📁 Структура проекта
my_site/
├── blog/                          # Приложение для блог-постов
│   ├── migrations/               # Миграции базы данных
│   ├── static/blog/              # Стили CSS для блога
│   │   ├── custom.css            # Пользовательские стили
│   │   └── main.css              # Основные стили сайта
│   ├── templates/blog/           # HTML-шаблоны для блога
│   │   ├── about.html            # Страница "О проекте"
│   │   ├── base.html             # Базовый шаблон, от которого наследуются другие
│   │   ├── home.html             # Главная страница с лентой постов
│   │   ├── post_confirm_delete.html # Подтверждение удаления поста
│   │   ├── post_detail.html      # Детальная страница поста
│   │   ├── post_form.html        # Форма создания/редактирования поста
│   │   └── user_posts.html       # Посты, написанные конкретным пользователем
│   ├── __init__.py
│   ├── admin.py                  # Регистрация моделей в админке
│   ├── apps.py                   # Конфигурация приложения
│   ├── forms.py                  # Форма для создания и редактирования постов
│   ├── models.py                 # Модель поста
│   ├── tests.py                  # Тесты для приложения блога
│   ├── urls.py                   # URL-маршруты блога
│   └── views.py                  # Представления (логика отображения страниц)
│
├── media/                         # Медиафайлы (аватары пользователей)
│   └── profile_pics/
│       └── default.jpg           # Аватар по умолчанию
│
├── my_site/                       # Основная конфигурация проекта
│   ├── __init__.py
│   ├── asgi.py                   # ASGI-конфигурация
│   ├── settings.py               # Основные настройки Django
│   ├── urls.py                   # Глобальные маршруты проекта
│   └── wsgi.py                   # WSGI-конфигурация
│
├── users/                         # Приложение для управления пользователями
│   ├── migrations/
│   ├── templates/users/          # HTML-шаблоны для аутентификации и профиля
│   │   ├── login.html            # Страница входа
│   │   ├── logout.html           # Страница выхода
│   │   ├── profile.html          # Страница профиля пользователя
│   │   └── register.html         # Страница регистрации нового пользователя
│   ├── __init__.py
│   ├── admin.py                  # Регистрация модели профиля в админке
│   ├── apps.py                   # Конфигурация приложения
│   ├── forms.py                  # Формы для регистрации и редактирования профиля
│   ├── models.py                 # Модель профиля пользователя
│   ├── signals.py                # Сигналы для автоматического создания профиля
│   ├── tests.py                  # Тесты для приложения users
│   └── views.py                  # Представления для регистрации, входа и профиля
│
├── manage.py                     # Django CLI
├── posts.json                    # Файл с постами (пример/экспорт)
├── .gitignore                    # Исключения для Git
├── README.md                     # Документация проекта
└── requirements.txt              # Список зависимостей

<pre> my_site/ ├── blog/ │ ├── migrations/ │ ├── static/blog/ │ │ ├── custom.css │ │ └── main.css │ ├── templates/blog/ │ │ ├── about.html │ │ ├── base.html │ │ ├── home.html │ │ ├── post_confirm_delete.html │ │ ├── post_detail.html │ │ ├── post_form.html │ │ └── user_posts.html │ ├── __init__.py │ ├── admin.py │ ├── apps.py │ ├── forms.py │ ├── models.py │ ├── tests.py │ ├── urls.py │ └── views.py │ ├── media/ │ └── profile_pics/ │ └── default.jpg │ ├── my_site/ │ ├── __init__.py │ ├── asgi.py │ ├── settings.py │ ├── urls.py │ └── wsgi.py │ ├── users/ │ ├── migrations/ │ ├── templates/users/ │ │ ├── login.html │ │ ├── logout.html │ │ ├── profile.html │ │ └── register.html │ ├── __init__.py │ ├── admin.py │ ├── apps.py │ ├── forms.py │ ├── models.py │ ├── signals.py │ ├── tests.py │ └── views.py │ ├── manage.py ├── posts.json ├── .gitignore ├── README.md └── requirements.txt </pre>

🛠 Используемые зависимости (requirements.txt)
Django>=4.0,<5.0
pillow
django-crispy-forms
bootstrap 4-5

💡 Идеи для развития
Комментарии к постам
Система лайков
Подписки на авторов
REST API (с использованием Django REST Framework)