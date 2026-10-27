# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django Application to store and retrieve data from a Vehicle Service Database platform using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
models.py
```

from django.db import models

class jayapradan(models.Model):
    order_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    customer_phone = models.CharField(max_length=15)
    restaurant_name = models.CharField(max_length=100)
    food_item = models.CharField(max_length=100)
    quantity = models.IntegerField()
    price = models.DecimalField(max_digits=8, decimal_places=2)
    total_amount = models.DecimalField(max_digits=10, decimal_places=2)
    delivery_address = models.TextField()
    payment_method = models.CharField(max_length=20)
    order_status = models.CharField(max_length=20)
    order_date = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return str(self.order_id)
```
admin.py
```

from django.contrib import admin
from .models import jayapradan

class jayapradanadmin(admin.ModelAdmin):
    list_display = [
        'order_id',
        'customer_name',
        'customer_phone',
        'restaurant_name',
        'food_item',
        'quantity',
        'price',
        'total_amount',
        'delivery_address',
        'payment_method',
        'order_status',
        'order_date'
    ]

admin.site.register(jayapradan, jayapradanadmin)
```


## OUTPUT


<img width="1531" height="817" alt="image" src="https://github.com/user-attachments/assets/6d652760-55a0-4b03-976d-e441d86023e2" />



## RESULT
Thus the program for creating vehicle service Database using ORM hss been executed successfully.
