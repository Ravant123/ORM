# Ex02 Django ORM Web Application
## Date: 14-12-2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM


![alt text](<ER diagram.jpg>)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin
class Bank_loan (models.Model):
    customer_id=models.IntegerField(primary_key=True)
    customer_name=models.CharField(max_length=100)
    loan_amount=models.IntegerField()
    customer_age=models.IntegerField()
    email=models.EmailField()

class Bank_loanAdmin(admin.ModelAdmin):
    list_display=('customer_id','customer_name','loan_amount','customer_age','email')


admin.py

from django.contrib import admin
from .models import Bank_loan,Bank_loanAdmin
admin.site.register(Bank_loan,Bank_loanAdmin)
```


## OUTPUT

Include the screenshot of your admin page.

![alt text](<Screenshot (79).png>)


![alt text](<Screenshot (80).png>)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
