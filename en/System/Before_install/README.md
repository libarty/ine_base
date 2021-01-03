# Before install

Main
	For all
		pip install Pillow # for working with images, converting to webm
		Django Rest Framework
			pip install djangorestframework # for connection to client
			pip install djoser # for create enter,exit and registrations
			pip install djangorestframework_simplejwt  # for create Token
			pip install django-filter # for filter content

	For each
		For Server
			For django
				pip install django # main addon
				pip install django-modeltranslation # for translate templates on saite
			For heroku
				pip install gunicorn # for work server in heroku
				pip install whitenoise # for working with static files
				pip install psycopg2 # for create database sql in heroku
				pip install dj-database-url # for work with the database in heroku
		For Client
			pip install pyinstaller # exe file conversion program
			Interface-QT
				pip install PyQT5 # for create a interface
				pip install PySide2 # alternative editor
				pip install PyQtWebEngine # for work with html
			Save files
				pip install mega.py # for work with MEGA 
				
			Auto-translator
				pip install googletrans # google translator
				pip install opencv-python # for highlight text
				pip install pytesseract # extracting text from a picture