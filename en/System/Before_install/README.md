# Before install

- Main
	- For all
		+ pip install Pillow # for working with images, converting to webm
		- Django Rest Framework
			+ pip install djangorestframework # for connection to client
			+ pip install djoser # for create enter,exit and registrations
			+ pip install djangorestframework_simplejwt  # for create Token
			+ pip install django-filter # for filter content
	- For each
		- For Server
			- For django
				+ pip install django # main addon
				+ pip install django-modeltranslation # for translate templates on saite
			- For heroku
				+ pip install gunicorn # for work server in heroku
				+ pip install whitenoise # for working with static files
				+ pip install psycopg2 # for create database sql in heroku
				+ pip install dj-database-url # for work with the database in heroku
		- For Client
			+ pip install pyinstaller # exe file conversion program
			- Interface-QT
				+ pip install PyQT5 # for create a interface
				+ pip install PySide2 # alternative editor
				+ pip install PyQtWebEngine # for work with html
			- Converter
				- Text
					+ pip install pypandoc
					+ pip install pdf2docx 
					+ install pandoc-2.11.3.2-windows-x86_64.msi
					+ install MiKTeX  # for work with pdf. Also you need run PowerShell and enter "name file.md" --pdf-engine = xelatex -o "name file.pdf" after install some packages 
				- Image 
					+ pip install Pillow
					+ pip install wand
					+ install ImageMagick-7.0.10-56-Q16-HDRI-x64-dll.exe
					+ install gs9533w64.exe # for work with pdf.
				- Video
					+ pip install moviepy
					+ pip install ffmpy
			- Save files
				+ pip install mega.py # for work with MEGA 
				
			- Auto-translator
				+ pip install googletrans # google translator
				+ pip install opencv-python # for highlight text
				+ pip install pytesseract # extracting text from a picture
				+ install tesseract-ocr-w64-setup-v5.0.0-alpha.20201127.exe # if 