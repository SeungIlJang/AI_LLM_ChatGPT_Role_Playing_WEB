# AI_LLM_ChatGPT_Role_Playing_WEB

### Explanation
- LLM(Large Language Model)
- TTS(Text to Speech)
- gTTS: Crawling Library
  
### Used Item
- Python 
- openai
- GPT-4
- pygame
- load_dotenv
- gTTS

![image](https://github.com/SeungIlJang/AI_LLM_ChatGPT_Role_Playing_WEB/assets/45052948/bde68a4b-b244-4f47-8111-56944ddb9edb)


![image](https://github.com/SeungIlJang/AI_LLM_ChatGPT_Role_Playing_WEB/assets/45052948/c999a44e-eac1-4e73-83a2-39da0978f549)

### Reference
#### Enable virtual environment
- ./venv/Scripts/activate

- pip install django==4.2.1 --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --trusted-host pypi.org
- pip install python-dotenv==1.0.0 --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --trusted-host pypi.org

#### 1) Navigate to the path you want to create the project.
#### 2) If you need to activate the virtual environment, please do it.
- cd ~/workspace/django-channels-gpt-role-playing

#### 3) Create a Django project in the current path.
#### Don't miss a period (.) at the end of a command.
- python -m djang startproject mysite .
#### Create Default Database
- python manage.py migrate 
#### Create the first superuser user/1234
- python manage.py createsuperuser

#### 4) Create a chat app
- python manage.py startapp chat

#### 5) settings.INSTALLED_APPS add "chat"
INSTALLED_APPS = [
	# ...
	"chat"
 ]

#### 6) Create chat/urls.py file
- from django.urls import path
- from . import views
- urlpatterns = []

#### 7) Integrated into mysite/urls.py
- from django.contrib impot adimn
- from django.urls import paht, include

urlpatterns = [
	# ...
	path("",include("chat.urls"))
]

#### Ensure that environmental variables are well reflected in long-range settings
- python manage.py shell
- from django.conf import settings
- settings.OPENAI_API_KEY

#### Create database chat/models.py
- python manage.py makemigrations chat
#### Reflect database chat/models.py- 
- python manage.py migrate chat
##### >python
##### >>>from chat.translators import google_translate
##### >>>google_translate("Hello World", "auto", "en")

#### Run Server
##### >python manage.py runserver
