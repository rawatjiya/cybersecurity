# Introduction to Cybersecurity Project 1 

This is the repository for the Introduction to Cybersecurity Project 1 demo django web application. The project is a 
simple Django-based notes application that allows users to register, login, create, view and search documents.
The applications backend intentionally has security vulnerabilities based on the OWASP 2021 Top 10 list for educational purposes. 

## Installation and Setup 

1. Clone the repository
```
git clone https://github.com/rawatjiya/cybersecurity-project-1.git
cd cybersecurity-project-1
```
2. Create a virtual environment and activate

```
python -m venv venv
```
(macOS/Linux)
```
source venv/bin/activate
```
(Windows)
```
venv\Scripts\activate
```
3. Install dependencies
```
pip install -r requirements.txt
```
4. Apply migrations
```
python manage.py migrate
```
5. Run server
```
python manage.py runserver
```

### Authentication Note 

This project deliberately includes an insecure authentication implementation, which means that existing users stored in the 
database may not authenticate correctly when testing. For replicability, the following steps are recommended: 

1. Ensure a clean and fully working environment
```
rm db.sqlite3
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```
2. Register new users through the application interface

After resetting the database and applying the migrations all features operate normally. 

### Testing the application

1. Register new users
2. Log in with valid credentials
3. Create notes
4. Search notes
5. Open detailed note pages

To test vulnerabilities, refer to the project report. 




