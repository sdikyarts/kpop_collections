<h2>Data Mahasiswa</h2>
Nama    : Yasmine Putri Viryadhani
<br>
NPM     : 2206081862
<br>
Kelas   : PBP A
<br>
<br>

<h2>Deskripsi Tugas</h2>
Nama App            : K-Pop Collections
<br>
Link App Adaptable  :
<br>
Link Repository     : https://github.com/sdikyarts/kpop_collections.git
<br>
<br>

<h2>Checklist Tugas</h2>
<h3>Proses pengimplementasian Checklist Tugas:<h3>
<h4>1. Membuat proyek Django</h4>
<dl>
    <dt>* Inisiasi Direktori Lokal</dt>
        <dd>- Sebelum membuat proyek Django, dibuatlah sebuah direktori kosong baru di lokal. Saya menamainya sebagai <code>kpop_collections</code></dd>
        <dd>- Setelah membuat direktori, kita harus menginisiasi repositori Git kosong di direktori tersebut dengan perintah <code>git_init</code></dd>
        <dd>- Lalu, kita harus mengkonfigurasi username dan email GitHub ke repositori Git tersebut di Terminal (MacOS) dengan cara:</dd>
        <dl>
            <dt>
                    <dd><code>git config user.name "<NAME>"</code></dd>
                <dd><code>git config user.email "<EMAIL>"</code></dd>
            </dt>
        </dl>
        <dd>- Kita juga bisa mengkonfigurasi secara global dengan cara:</dd>
        <dl>
            <dt>
                <dd><code>git config --global user.name "<NAME>"</code></dd>
                <dd><code>git config --global user.email "<EMAIL>"</code></dd>
            </dt>
        </dl>
        <dd>- Verifikasi git lokal</dd>
        <dl>
            <dt>    
                    <dd><code>git config --list --local</code></dd>
            </dt>
        </dl>
    <dt>* Membuat repository baru di GitHub<dt>
        <dd>
            <spoiler><img src="repo_fresh.png" alt="tampilan repository"></spoiler>
        </dd>
    </dt>
    <dt>* Instalasi + Inisiasi Django pada repository</dt>
        <dd>- Menambahkan virtual environment ke dalam directory <code>kpop_collections</code> dengan menjalankan kode <code>python3 -m venv env</code> (di MacOS)</dd>
        <dd>- Menjalankan virtual environment dengan cara 
        <dl>
            <dt>MacOS</dt>
                <dd><code>source env/bin/activate</code></dd>
        </dl>
        <dd>- Menyiapkan Dependencies dengan membuat berkas <code>requirements.txt</code> di directory yang sama, lalu menambahkan
        <dl>
            <dt>
                <dd><code>
                    django
                    gunicorn
                    whitenoise
                    psycopg2-binary
                    requests
                    urllib3
                </code></dd>
            </dt>
        </dl>
        ke dalam berkas <code>requirements.txt</code></dd>
        <dd>- Install dependencies dengan menjalankan
        <dl>
            <dt>
                <dd><code>
                    pip install -r requirements.txt
                </code></dd>
            </dt>
        </dl></dd>
        <dd>- Buat proyek Django dengan nama <code>kpop_collections</code> dengan menjalankan perintah <code>django-admin startproject kpop_collections .</code></dd>
        <dd>- Tambahkan <code>*</code> pada <code>ALLOWED HOSTS</code> di <code>settings.py</code></dd>
        <dl>
            <dt>
                <dd><code>
                    ...
                    ALLOWED_HOSTS = ["*"]
                    ...
                </code></dd>
            </dt>
        </dl>
        <dd>- Setelah memastikan file <code>manage.py</code> ada di directory, jalankan instruksi <code>./manage.py runserver</code> (MacOS). Saat menjalankan domain http://localhost:8000 muncul animasi roket</dd>
        <dd>
            <spoiler><img src="success install django.png" alt="tampilan repository"></spoiler>
        </dd>
    <dt>* Push ke repository GitHub</dt>   
        <dd>- Buat file <code>.gitignore</code> (masih di directory <code>kpop_collections</code>), lalu isi dengan
        <spoiler>
            <code> 
# Django
*.log
*.pot
*.pyc
__pycache__
db.sqlite3
media

# Backup files
*.bak 

# If you are using PyCharm
# User-specific stuff
.idea/**/workspace.xml
.idea/**/tasks.xml
.idea/**/usage.statistics.xml
.idea/**/dictionaries
.idea/**/shelf

# AWS User-specific
.idea/**/aws.xml

# Generated files
.idea/**/contentModel.xml

# Sensitive or high-churn files
.idea/**/dataSources/
.idea/**/dataSources.ids
.idea/**/dataSources.local.xml
.idea/**/sqlDataSources.xml
.idea/**/dynamic.xml
.idea/**/uiDesigner.xml
.idea/**/dbnavigator.xml

# Gradle
.idea/**/gradle.xml
.idea/**/libraries

# File-based project format
*.iws

# IntelliJ
out/

# JIRA plugin
atlassian-ide-plugin.xml

# Python
*.py[cod] 
*$py.class 

# Distribution / packaging 
.Python build/ 
develop-eggs/ 
dist/ 
downloads/ 
eggs/ 
.eggs/ 
lib/ 
lib64/ 
parts/ 
sdist/ 
var/ 
wheels/ 
*.egg-info/ 
.installed.cfg 
*.egg 
*.manifest 
*.spec 

# Installer logs 
pip-log.txt 
pip-delete-this-directory.txt 

# Unit test / coverage reports 
htmlcov/ 
.tox/ 
.coverage 
.coverage.* 
.cache 
.pytest_cache/ 
nosetests.xml 
coverage.xml 
*.cover 
.hypothesis/ 

# Jupyter Notebook 
.ipynb_checkpoints 

# pyenv 
.python-version 

# celery 
celerybeat-schedule.* 

# SageMath parsed files 
*.sage.py 

# Environments 
.env 
.venv 
env/ 
venv/ 
ENV/ 
env.bak/ 
venv.bak/ 

# mkdocs documentation 
/site 

# mypy 
.mypy_cache/ 

# Sublime Text
*.tmlanguage.cache 
*.tmPreferences.cache 
*.stTheme.cache 
*.sublime-workspace 
*.sublime-project 

# sftp configuration file 
sftp-config.json 

# Package control specific files Package 
Control.last-run 
Control.ca-list 
Control.ca-bundle 
Control.system-ca-bundle 
GitHub.sublime-settings 

# Visual Studio Code
.vscode/* 
!.vscode/settings.json 
!.vscode/tasks.json 
!.vscode/launch.json 
!.vscode/extensions.json 
.history
            </code>
        </spoiler></dd>
        <dd>- Add, commit, dan Push ke repository GitHub</dd>
<dl>