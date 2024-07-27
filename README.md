# django-weather-app

## Links
- https://blog.jetbrains.com/pycharm/2023/04/create-a-django-app-in-pycharm/
- https://github.com/denis-mashutin/weather-app-tutorial/tree/main?tab=readme-ov-file

- https://geocoder.readthedocs.io/
- https://docs.djangoproject.com/en/4.1/ref/settings/#std-setting-TIME_ZONE

- https://api.open-meteo.com/v1/forecast
- https://www.kaggle.com/datasets/juanmah/world-cities
- https://www.sqlite.org/datatype3.html
- https://www.geeksforgeeks.org/import-a-csv-file-into-an-sqlite-table/

- https://simplecss.org/
- https://getbootstrap.com/docs/5.3/getting-started/introduction/#quick-start
- https://getbootstrap.com/docs/5.3/getting-started/introduction/

- http://127.0.0.1:8000/meteo/discover

## Commands
- pip install django
- pip install python-dotenv
- pip install requests # or use pycharm install
- pip install geocoder # or use pycharm install
- django-admin startproject core .
- python manage.py startapp meteo
- python manage.py inspectdb worldcities

## Commands 2
- python manage.py shell
- run views.py in shell
- temp_here()
- temp_here()['hourly']['temperature_2m'][14]

## Commands 3
```
CREATE TABLE "worldcities" (
	"city"	TEXT,
	"lat"	REAL,
	"lng"	REAL,
	"country"	TEXT,
	"id"	INTEGER NOT NULL,
	PRIMARY KEY("id" AUTOINCREMENT)
);
```

## Commands 4
- Replace null=True with primary_key=True for the id field
```
django-weather-app % python manage.py inspectdb worldcities
# This is an auto-generated Django model module.
# You'll have to do the following manually to clean this up:
#   * Rearrange models' order
#   * Make sure each model has one field with primary_key=True
#   * Make sure each ForeignKey and OneToOneField has `on_delete` set to the desired behavior
#   * Remove `managed = False` lines if you wish to allow Django to create, modify, and delete the table
# Feel free to rename the models, but don't rename db_table values or field names.
from django.db import models


class Worldcities(models.Model):
    city = models.TextField(blank=True, null=True)
    lat = models.FloatField(blank=True, null=True)
    lng = models.FloatField(blank=True, null=True)
    country = models.TextField(blank=True, null=True)

    class Meta:
        managed = False
        db_table = 'worldcities'

```