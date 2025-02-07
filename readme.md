# lernbaustein erweitert - python

In diesem Repository lieg Beispielcode fuer einen erweiterten Lernbaustein zum Thema Python.
    - Erstellen eines Wiederverwendbaren Django-App
    - Packetieren und Hochladen in ein Packet-Repository
    - Erstellen eines Dockerimages

## Erstellen eines importierbaren Pythonpackets

Mit Django ist es moeglich Apps auszulagern

    https://docs.djangoproject.com/en/5.1/intro/reusable-apps/

## Packetieren einer Pythonanwendung

Das Packetieren und ausliefern eines Pythonpackets ist unter folgendem Link beschrieben

    https://packaging.python.org/en/latest/tutorials/packaging-projects/#uploading-the-distribution-archives

#### Packet erstellen

Das Verzeichnis django-skillprofil/ enthaelt eine funktionsfaehige Django-App.
Siehe dazu auch

    https://github.com/Philipp-Co/conciso-kickstarter-python

Im Verzeichnis django-skillprofil

    python -m build --sdist

Durch das Kommando entsteht ein Verzeichnis dist/
in diesem Verzeichnis liegen die erstellten Pythonpackete.
Um das Packet zu verteilen sollte die pyproject.toml angepasst werden,
zumindest die Versionsnummer fuer das neu erstellte oder angepasste 
Packet. Dann kann mit 

    python -m twine upload --repository pypi dist/*

ein Upload erfolgen, hier zu pypi. 


Siehe auch:
|               Links                                                   |
|-----------------------------------------------------------------------|
| https://build.pypa.io/en/stable/                                      |
| https://packaging.python.org/en/latest/guides/writing-pyproject-toml/ |

### Eine Anwendung erstellen

Im Verzeichnis lep/ befindet sich ein Django-Projekt ohne weitere Apps.
Die Django-App django-skillprofil ist hier als externes Packet ueber die requirements/production.txt eingebunden.

    ./manage.py makemigrations django-skillprofil --settings lep.setting
    ./manage.py migrate --settings lep.setting
    ./manage.py runserver 0.0.0.0:8000 --settings lep.settings

### Docker

TBD
    - staged builds
    - alpine image

## Packete Komprimieren

TBD
    - https://pypi.org/project/python-minifier/
