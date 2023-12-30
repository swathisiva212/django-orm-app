# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
clone the problem from github
### STEP 2:
create a new app
### STEP 3:
enter the code admin.py and model.py
### step4:
execute a django admin and create a 10 employees

## PROGRAM
Model.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()


class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

Admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)



## OUTPUT
![image](https://github.com/swathisiva212/django-orm-app/assets/155249892/8ae24fa8-ad6f-4b05-ae82-5c0dada4ba7b)




## RESULT
program executed sucessfully.
