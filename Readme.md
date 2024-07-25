# To create module

```
custom modules/
└── hotel_management/
    ├── __manifest.py__
    └── __init.py__
```
> add json format in manifest
```
{
    'name':'Hotel Management'
}
```

> turn on active developer mode

> update app list

# To creat a icon of module 
```
custom modules/
├── hotel_management
└── static/
    ├── description/
    │   └── icon.png
    ├── __manifest.py__
    └── __init.py__
```
> then upgrade the module


# To create a database Model
```sh
custom modules/
└── hotel_management/
    ├── models/
    │   ├── guests.py
    │   └── __init.py__
    ├── static/
    │   └── description/
    │       └── icon.png
    ├── __manifest.py__
    └── __init.py__
```
>guests.py

```
from odoo import api, models, fields,

class HotelGuests(models.Model):
    _name = 'hotel.guests'
    _description = 'Hotel Guests'

    ref = fields.Char(string='Ref')

```







    
