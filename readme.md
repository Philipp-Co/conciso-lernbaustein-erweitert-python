# lernbaustein erweitert - python

In diesem Repository lieg Beispielcode fuer einen erweiterten Lernbaustein zum Thema Python.
    - Erstellen eines Wiederverwendbaren Django-App
    - Packetieren und Hochladen in ein Packet-Repository
    - Erstellen eines One-File-Executables
    - Erstellen eines Dockerimages

## Erstellen eines importierbaren Pythonpackets

https://docs.djangoproject.com/en/5.1/intro/reusable-apps/

## Packetieren einer Pythonanwendung

https://packaging.python.org/en/latest/tutorials/packaging-projects/#uploading-the-distribution-archives

#### Packet erstellen

Im Verzeichnis django-skillprofil

    python -m build

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

### One-File-Executable

TBD

### Docker

TBD

## Packete Komprimieren

TBD
