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

### 참고사항
#### 가상환경 활성화
- ./venv/Scripts/activate

- pip install django==4.2.1 --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --trusted-host pypi.org
- pip install python-dotenv==1.0.0 --trusted-host pypi.python.org --trusted-host files.pythonhosted.org --trusted-host pypi.org

#### 1) 프로젝트 생성할 경로로 이동합니다.
#### 2) 가상환경 활성화가 필요하다면 해주세요.
- cd ~/workspace/django-channels-gpt-role-playing

#### 3)현재 경로에 장고 프로젝트를 생성합니다.
#### 명령 끝에 마침표(.)를 빼먹지 마세요.
- python -m djang startproject mysite .
#### 디폴트 데이터 베이스 생성
- python manage.py migrate 
#### 첫 superuser를 생성 terry/79jasi
- python manage.py createsuperuser

#### 4) chat 앱 생성
- python manage.py startapp chat

#### 5) settings.INSTALLED_APPS에 "chat"추가
INSTALLED_APPS = [
	# ...
	"chat"
 ]

#### 6) chat/urls.py 파일생성
- from django.urls import path
- from . import views
- urlpatterns = []

#### 7) mysite/urls.py에 통합
- from django.contrib impot adimn
- from django.urls import paht, include

urlpatterns = [
	# ...
	path("",include("chat.urls"))
]

#### 환경변수가 장고 setttings에 잘 반영되었는지 확인
- python manage.py shell
- from django.conf import settings
- settings.OPENAI_API_KEY

#### database 생성 chat/models.py
- python manage.py makemigrations chat
#### database 반영 chat/models.py- 
- python manage.py migrate chat
##### >python
##### >>>from chat.translators import google_translate
##### >>>google_translate("Hello World", "auto", "en")

#### 서버구동
##### >python manage.py runserver
