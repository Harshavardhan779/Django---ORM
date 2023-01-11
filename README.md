# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
create a simple table using table tag

### STEP 2:
Add header row using the tag

### STEP 3:
Add your timetable

## PROGRAM

```html
admin.py:

from django.contrib import admin
from .models import Student,StudentAdmin


admin.site.register(Student,StudentAdmin)

manage.py:

from django.db import models
from django.contrib import admin
# Create your models here.

class Student(models.Model):
    referencenumber=models.CharField(max_length=10,help_text="Your Reference Number")
    name=models.CharField(max_length=100)
    department=models.CharField(max_length=200)
    age=models.IntegerField()
    email=models.EmailField()

class StudentAdmin(admin.ModelAdmin):
    list_display = ('referencenumber','name','age','department','email')
# Register your models here.
```

## OUTPUT

![MODEL](/WhatsApp%20Image%202023-01-11%20at%2022.19.22.jpeg)


## RESULT
Timetable is created sucessfully.

