# Ex02 Django ORM Web Application
# Date: 1.11.2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
1.models.py
```
from django.db import models
from django.contrib import admin

class book(models.Model):
    book_no = models.AutoField(primary_key=True)  
    book_name = models.CharField(max_length=200)  
    customer_name = models.CharField(max_length=100) 
    mobile_no = models.CharField(max_length=15)  
    email = models.EmailField()  
    book_price = models.DecimalField(max_digits=10, decimal_places=2)  
    aadhar_no = models.CharField(max_length=12, blank=True, null=True) 
    address = models.TextField(blank=True, null=True) 
class Admin(admin.ModelAdmin):
    list_display = ('book_no', 'book_name', 'customer_name', 'mobile_no', 'email', 'book_price', 'aadhar_no', 'address')

2.admin.py

from django.contrib import admin
from .models import book, Admin
admin.site.register(book, Admin)

# OUTPUT
```


![Screenshot (21)](https://github.com/user-attachments/assets/9d75c8b3-c1bd-4993-8d70-35d488142c94)
![Screenshot (15)](https://github.com/user-attachments/assets/e219078a-078d-4ed5-b4c8-5023ec77da9b)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
