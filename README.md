# 📝 Django Blog Project(Grim)

Полноценный блог на Django, разработанный как гибкая и расширяемая основа для любого проекта — от персонального дневника до корпоративного новостного портала.

## 📌 О проекте

Этот блог — это не просто учебный шаблон, а настоящая база для запуска собственного онлайн-продукта. Он построен с учётом масштабируемости и лёгкости интеграции с другими сервисами — будь то веб-интерфейс, мобильное приложение или Telegram-бот.  

Проект идеально подходит:  
- Для персонального блога или портфолио  
- Для блога небольшой компании или стартапа  
- Как CMS-ядро для Telegram-бота (например, бот, публикующий посты или уведомления)  
- Для тестирования интеграции Django с внешними API  
- Как стартовая точка для изучения Django + пользователей + медиа  

---

### 📌 Особенности проекта  
- Регистрация, вход и выход пользователей  
- Профиль с возможностью загрузки аватара  
- Создание, редактирование и удаление постов  
- Просмотр всех постов и постов отдельного пользователя  
- Чистый, адаптивный интерфейс на Bootstrap  

---

## 🔧 Технологии

| Категория     | Технологии                       |
|---------------|----------------------------------|
| Язык          | Python 3                         |
| Фреймворк     | Django                           |
| UI            | HTML, CSS, Bootstrap 4-5           |
| Формы         | Django Crispy Forms              |
| Работа с медиа| Pillow                           |
| База данных   | SQLite (по умолчанию)            |

---

## 🚀 Установка и запуск

### 1. Клонируйте репозиторий

```bash
git clone https://github.com/yourusername/django-blog.git
cd django-blog
```
### 2. Создайте и активируйте виртуальное окружение  
```
python -m venv venv  
source venv/bin/activate  # для Linux/macOS  
venv\Scripts\activate     # для Windows  
```
### 3. Установите зависимости  
```
pip install -r requirements.txt  
```
### 4. Примените миграции и создайте суперпользователя  
```
python manage.py migrate
python manage.py createsuperuser
```
### 5. Запустите сервер  
```
python manage.py runserver  
```
Перейдите по адресу: http://127.0.0.1:8000  

### 📁 Структура проекта  
```
my_site/
├── blog/                          
│   ├── migrations/               
│   ├── static/blog/              
│   │   ├── custom.css            
│   │   └── main.css              
│   ├── templates/blog/           
│   │   ├── about.html            
│   │   ├── base.html             
│   │   ├── home.html             
│   │   ├── post_confirm_delete.html
│   │   ├── post_detail.html      
│   │   ├── post_form.html        
│   │   └── user_posts.html       
│   ├── admin.py                  
│   ├── apps.py                   
│   ├── forms.py                  
│   ├── models.py                 
│   ├── urls.py                   
│   └── views.py                  
│
├── media/                         
│   └── profile_pics/
│       └── default.jpg           
│
├── my_site/                       
│   ├── __init__.py
│   ├── asgi.py                   
│   ├── settings.py               
│   ├── urls.py                   
│   └── wsgi.py                   
│
├── users/                         
│   ├── migrations/
│   ├── templates/users/          
│   │   ├── login.html            
│   │   ├── logout.html           
│   │   ├── profile.html          
│   │   └── register.html         
│   ├── admin.py                  
│   ├── apps.py                   
│   ├── forms.py                  
│   ├── models.py                 
│   ├── signals.py                
│   ├── urls.py                   
│   └── views.py                  
│
├── manage.py                     
├── posts.json                    
├── .gitignore                    
├── README.md                     
└── requirements.txt              
```  
## 🛠 Зависимости  
- Django>=4.0,<5.0  
- pillow  
- django-crispy-forms  
- bootstrap 4-5  

## 💡 Идеи для развития:  

- Комментарии к постам  
- Система лайков  
- Подписки на авторов  
- REST API (Django REST Framework)  
- Интеграция с Telegram-ботом  
- Уведомления о новых постах  


