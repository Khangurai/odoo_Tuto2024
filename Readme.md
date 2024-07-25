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
from odoo import api, models,fields

class HotelGuests(models.Model):
    _name = 'hotel.guests'
    _description = 'Hotel Guests'

    ref = fields.Char(string='Ref')
    name = fields.Char(string='Name')
    dob = fields.Datetime(string='Date of Birth')
    age = fields.Integer(string='Age')
    gender = fields.Selection([('male','Male'), ('female','Female')], string='Gender')
    active = fields.Boolean(string='Active', default = True)
```
>models/init py
```
from . import guests
```

>main init file
```
from . import models
```
- to check in settings\technical\database\models
- to check in models in database
- open terminal
```
psql -U postgres -d demo_db
```
- username - postgres
- database - demo_db
- you can aslo check in pgadmin4
- select database `demo_db` and type query 
```
psql -U postgres -d demo_db
```
>and type query
```
select * from hotel_guests
```
# To create menu
```
custom modules/
└── hotel_management/
    ├── views/
    │   └── menu.xml
    ├── models/
    │   ├── guests.py
    │   └── __init.py__
    ├── static/
    │   └── description/
    │       └── icon.png
    ├── __manifest.py__
    └── __init.py__
```    
in xml file 
```
<?xml version="1.0" encoding="utf-8"?>
<odoo>
    <menuitem id=""
              name=""
              sequence="0"/>

</odoo>
```
ဒီအထိကမပေါ်သေးဘူး  menu မှာ 

`menu`မှာပေါ်ချင်ရင်settings\user interface\menu items မှာပြင်ပေးမှ ရမယ်

check this [youtube](https://www.youtube.com/watch?v=jdsP7RQ-8Hs&list=PLqRRLx0cl0hoZM788LH5M8q7KhiXPyuVU&index=7) how to create sub menu

>[!NOTE]
>တစ်ခုနဲ့တစ်ခုကို link ချိတ်ပေးရမယ်
>
>တစ်ခုခုပေါ်အောင်action တစ်ခုထည့်ပေး

    
