# Projeto DJANGO

# Pre-requsito

	C:\python --version
	
	# Ver se o Virtualenv já está instalado
	C:\where virtualenv

	# Instalar um pacote apenas para o usuário atual
	
	#Install virtualenv and virtualenvwrapper
	C:\pip install virtualenv 
	C:\pip install virtualenvwrapper-win
	
	ou
	
	C:\python -m pip install --user virtualenv

# Criação de uma pasta onde vamos guardar os ambientes virtuais, (utilizar o CMD)

C:\md projetodjango
C:\md projetodjango\venv
C:\cd \projetodjango\venv


# Criação do ambiente virutal (python -m, indica que somente será feita instalção para o usuario atual)
	
	C:\python -m venv [NOME DO SEU AMBIENTE VIRTUAL]
	
	# Caso a pasta ja esteja criada (created a virtual enviroment)
	C:\projetodjango\venv\virtualenv .

	# Criando a pasta 
	C:\projetodjango\python -m venv venv
	
	ou
	
	C:\projetodjango\python -m venv .venv

	# Atualizar pip
	C:\python -m pip install --upgrade pip
	
# Ativação do ambiente virtual

	# Pelo CMD
	[NOME DO AMBIENTE VIRTUAL]\Scripts\activate.bat
	C:\.\venv\Scripts\activate.bat
		
		# ambiente virtual ativado
		(venv) C:\projetodjango\venv>
	
	# Atravéss do PowerShell
	[NOME DO AMBIENTE VIRTUAL]\Scripts\activate.ps1
	C:\.\venv\Scripts\activate.ps1
		
		# ambiente virtual ativado
		(venv) C:\projetodjango\venv>
	

	Include: inicialmente vazia, é utilizada para armazenar arquivos header em C no caso de você instalar pacotes em Python que dependa de extensões em C. uma cópia da versão Python juntamente com a pasta site-packages onde cada dependência será instalada.
	Lib: contém bibliotecas padrão e é nela que serão armazenadas as bibliotecas específicas que você instalar para o seu projeto.
	Scripts: contém scripts Python para controle do seu ambiente virtual, como o interpretador Python da versão instalada e o pacote pip para instalação das bibliotecas de terceiros mencionadas.
	pyvenv.cfg: arquivo de configuração do seu ambiente virtual que contém chaves que indicam qual a versão do Python a ser instalada no ambiente (a mesma utilizada para criar o ambiente).
	bin:(Linux e MacOS) arquivos que interagem com o ambiente virtual.

# Desativar um ambiente virtual
C:\.\venv\Scripts\deactivate.bat

# Criar este ambiente virtual com uma versão do Python diferente
# Exemplo de ambiente virtual com o Python 3.7.9
C:\projetodjango\venv\virtualenv . --python=3.7.9

# Ambiente virtual com uma versão do Python que não esteja no path
# é preciso que se indique o caminho completo do Python executável.

C:\projetodjango\venv2\virtualenv . --python "C:\Program Files\Python3x\python.exe"

# Exibir todos os pacotes instalados no ambiente virtual
(venv) C:\projetodjango\venv>python -m pip list 

# Instalando o django
(venv) C:\projetodjango\venv>pip install django

# Verificação de versão
(venv) C:\projetodjango\venv>django-admin --version

# Iniciando o Projeto usando o django-admin
(venv) C:\projetodjango\venv>django-admin startproject venv

# Rodar o web server de desenvolvimento
(venv) C:\projetodjango\venv>manage.py runserver

# Verificar os pacotes no ambiente
(venv) C:\projetodjango\venv>pip list

'''
# Compartilhando um ambiente venv através da documentação das dependências do projeto
'''
# requirements.txt, lista as dependências de um projeto e as versões específicas de cada biblioteca utilizadas nele.

	# Lista os pacotes instalados em arquivo texto
	python -m pip freeze > requirements.txt

	# O arquivo requirements.txt pode ser submetido no controle de versão e adicionado como parte da aplicação. 
	python -m pip install -r requirements.txt

#

#VS Code	

#

The command presents a list of available interpreters that VS Code can locate automatically
Command Palette (View > Command Palette) or Ctrl+Shift+P --> Then select the Python: Select Interpreter command

#Run Terminal: Create New Terminal (Ctrl+Shift+`)
The selected environment appears on the right side of the VS Code status bar, and notices the ('.venv': venv) indicator that tells you that you're using a virtual environment

#In the VS Code Terminal where your virtual environment is activated, run the following command:
python -m pip install --upgrade pip
python -m pip install django

# Create the Django project In the VS Code Terminal

 Update the character set to utf8mb4 for full unicode support, utf8 is not the complete standard.
 
 
django-admin startproject web_project .

This startproject command assumes (by use of . at the end) that the current folder is your project folder, and creates the following within it:

	manage.py: The Django command-line administrative utility for the project. You run administrative commands for the project using python manage.py <command> [options].
	
	A subfolder named web_project, which contains the following files:

		__init__.py: an empty file that tells Python that this folder is a Python package.
		asgi.py: an entry point for ASGI-compatible web servers to serve your project. You typically leave this file as-is as it provides the hooks for production web servers.
		settings.py: contains settings for Django project, which you modify in the course of developing a web app.
		urls.py: contains a table of contents for the Django project, which you also modify in the course of development.
		wsgi.py: an entry point for WSGI-compatible web servers to serve your project. You typically leave this file as-is as it provides the hooks for production web servers.

Create an empty development database by running the following command:

python manage.py migrate

When you run the server the first time, it creates a default SQLite database in the file db.sqlite3 that is intended for development purposes, but can be used in production for low-volume web apps. For additional information about databases, see the Types of databases section.

To verify the Django project, make sure your virtual environment is activated, then start Django's development server using the command/;

python manage.py runserver. 

The server runs on the default port 8000, and you see output like the following output in the terminal window:

	Example the output in the terminal window:
	
		Performing system checks...

		System check identified no issues (0 silenced).

		January 15, 2021 - 14:33:31
		Django version 3.1.5, using settings 'web_project.settings'
		Starting development server at http://127.0.0.1:8000/
		Quit the server with CTRL-BREAK.
		
Django's built-in web server is intended only for local development purposes. When you deploy to a web host, however, Django uses the host's web server instead. The wsgi.py and asgi.py modules in the Django project take care of hooking into the production servers.

If you want to use a different port than the default 8000, specify the port number on the command line, such as python manage.py runserver 5000.

Ctrl+click the http://127.0.0.1:8000/ URL in the terminal output window to open your default browser to that address. If Django is installed correctly and the project is valid, you see the default page shown below. The VS Code terminal output window also shows the server log.

# Django MySQL Setup

# Connect Django to MySQL Using XAMPP

# On XAMPP install Apache, MariaDB and PhpMyAdmin

# Start the XAMPP Server
	
	Click the Start button for Apache, and the start button for MySQL

# Create A MySQL Database
	
	Note that the name you type here is the one you will use in Django’s settings.py file. The database is done, let’s connect to it from Django.

# Install A MySQL adapter In Your Django Project	

# Install the mysqlclient package of Python

	# MySQL adapters allow us to connect to MySQL from the Python side. 
	# The most popular and the fastest ones, which are mysqlclient and pymysql.

	(.env) C:\projetodjango\.env> pip install mysqlclient # or  Install pymysql in Your Django Project.
	
	-=> The (env) at the beginning indicates an activated virtual environment called env.
	
#  It is now time to tell Django to use MySQL instead of the default SQLite. We do this in our settings.py.

	-=> By default, Django wants to use MySQLCLient to make a connection with MySQL database, but because we used "mysqlclient or pymysql" in this case, we have to update our __init__.py file. 
	
	__init__.py
	
	import pymysql
	pymysql.install_as_MySQLdb()

# Connect To The Database From Django’s settings.py

 Change the DATABASES dictionary to look like this:

	WARNING: Use environmental variables to conceal the sensitive information
	
	DATABASES = {
		'default': {
			'ENGINE'	: 'django.db.backends.mysql',
			'NAME'		: 'database_name',
			'USER'		: 'root',
			'PASSWORD'	: '',
			'HOST'		: '127.0.0.1',
			'PORT'		: '3306',
			'OPTIONS'	: {'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"},
		}
	}
	
	# Understand what we have done above.

	First, we have replaced the 'django.db.backends.sqlite3' to 'django.db.backends.mysql'. This is basically indicating we shift SQLite to MySQL database.
	NAME indicates the name of the database we want to use.
	USER is the MYSQL username that has access to the Database and acts as a database administrator.
	PASSWORD is the password of the database. It will be created at the time of MySQL installation.
	'HOST' is '127.0.0.1' and 'PORT' '3306' points out that the MySQL databaseis hosted with the hostname '0.0.1' and listens to the specific port number is 3306.
	In the last line we use SET sql_mode = 'STATIC_TRANS_TABLES' which is used to handle the invalid or missing values from being stored in the database by INSERT and UPDATE statements.

	# Start the project (Make Migrations)
	
	-=> Now migration that will create all necessary tables.
	
	(env) C:\projetodjango\python manage.py makemigrations
	
	# Run the command to perform the migrations:
	
	(env) C:\projetodjango\>python manage.py migrate
	
	-=> This will migrate all the default Django tables to your MySQL schema.
	
	# After creating the database structure, we can create an administrative account
	
	(env) C:\projetodjango\>python manage.py createsuperuser
	
	# Start the application (development mode)
	
	(env) C:\projetodjango\>python manage.py runserver
	
		http://server_domain_or_IP:8000/admin
		
		
# To use Environment variables in a Django project

# Install python-dotenv

-=> Importing python-dotenv in our settings.py file

	C:\projetodjango\.env>pip install python-dotenv

# Create a .env file at the root of the Project

	At the root of your Django project folder, create a new file called .env
	
	The project structure should look like this:
	
	...
	|
	+--- .env  (In VS Code, it is displayed as a gear icon)
	|
	+--- manage.py
	
	or 

	PROJECT ROOT >
   |
   |-- manage.py         # Specify the settings file
   |
   |-- core/             # Implements app logic and serve the static assets
   |    |-- settings.py  # Django app bootstrapper
   |    |-- wsgi.py      # Start the app in production
   |    |-- urls.py      # Define URLs served by all apps/nodes

# Set Environment Variables in .env file

	A few variables that are important to keep safe
	
	SECRET_KEY=django-insecure-g6owp@47mbu33+nemhf$btj&6e7t&8)&n!uax1obkf-d)9$9*j
	DB_NAME=moviereviews
	DB_USER=root
	DB_PASS=hO5xY%00j
	
	# Development settings
	DOMAIN=example.org
	ADMIN_EMAIL=admin@${DOMAIN}
	ROOT_URL=${DOMAIN}/app

	-=> These are few of the variables you can add to the .env file.
	-=> Note that we don’t use quotes around strings because they will be converted automatically when they get loaded into the settings.py file.
	-=> Note that we also do not use spaces on both sides of the assignment operator because there is no need to.
	
# Assign the Environment Variables in the settings.py

	Its now time to replace the explicit values in the settings.py with the ones in the Django environment variable file

# Import and Initialise python-dotenv in settings.py

from dotenv import load_dotenv
import os

load_dotenv()


	# Use environ from os as follows:

	SECRET_KEY = os.environ.get('SECRET_KEY') #here
	...
	DATABASES = {
		'default': {
			'ENGINE': 'django.db.backends.mysql',
			'NAME': os.environ.get('DB_NAME'), #here
			'USER': os.environ.get('DB_USER'), #here
			'PASSWORD': os.environ.get('DB_PASS'), #here
			'HOST': '127.0.0.1',
			'PORT': '3306',
			'OPTIONS': {'init_command': "SET sql_mode='STRICT_TRANS_TABLES'"},
		}
	}

# Add the .env file to .gitignore file

# Generate Secret Key in Django Using get_random_secret_key() function

	This function gives back a string of 50 characters with random characters.
	
	Access the Python Interactive Shell
	
	(env) $ python manage.py shell
	
	Import the get_random_secret_key() function from django.core.management.utils.

	>>> from django.core.management.utils import get_random_secret_key
	
	Generate the Secret Key in the Terminal using the get_random_secret_key() function
	
	>>> print(get_random_secret_key())
		
		# The Random secret key will be generated on the next line like this:
		
		gw^9ej(l4vq%d_06xig$vw+b(-@#00@8l7jlv77=sq5r_sf3nu
	
	Copy and Paste the Key into your SECRET_KEY variable in the settings.py or 
	
	# SECURITY WARNING: keep the secret key used in production secret! 
	
	# You have to use environment variables
	
	SECRET_KEY = 'dgw^9ej(l4vq%d_06xig$vw+b(-@#00@8l7jlv77=sq5r_sf3nu'
	
# Generate Secret Key in Django Using Secret Key Generator (Djecrety on https://djecrety.ir/)
	
	-=> Go to the homepage and click on the generate button and it will generate the secret key for you. Copy the Key and use it as your Django Secret key