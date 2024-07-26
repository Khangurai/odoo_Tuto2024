# To create form view

add this code in guest_view.xml
```xml
<record id="view_hotel_guest_form" model="ir.ui.view">
            <field name="model">hotel.guest.form</field>
            <field name="model">hotel.guest</field>
            <field name="arch" type="xml">
                <form>
                    <group>
                        <field name = "name"/>
                        <field name = "age"/>
                        <field name = "gender"/>
                    </group>
                </form>
            </field>
     </record>
```
>in `<form>` tag you can easily create the format of form

**to view form `Settings\views`**

> [!TIP]
>if you create sheet view fom just create `<sheet>` tag between `<form>` and `<group>` tag

![ViewForm](https://github.com/Khangurai/odoo_Tuto2024/blob/main/assests/2.png)

>**to devide the form group like this** 

**add code in this section between `<group>` tag** 

```xml
<form>
    <sheet>
        <group>
            <group>
                <field name = "name"/>
                <field name = "age"/>
            </group>
            <group>
                <field name = "gender"/>
            </group>
        </group>
    </sheet>
</form>
```


------------

# How to define a Tree view

view form/list/tree တွေပြောင်းမယ်ဆိုရင် windows action ရဲ့  xml ထဲမှာ ပဲ့ပြောင်းရုံပဲ့ view type ပြောင်းရုံပဲ့

add befor the form view 
i think this view type is order by window action 
so you see the first one is tree view `(primary view)`
and then you add the record u'll see  `(form view)`
```xml
<record id="view_hotel_guest_tree" model="ir.ui.view">
            <field name="model">hotel.guest.tree</field>
            <field name="model">hotel.guest</field>
            <field name="arch" type="xml">
                <tree>
                    <field name = "name" string="Guest Name"/>
                    <field name = "age"/>
                    <field name = "gender"/>
                </tree>
            </field>
     </record>
```

------------

# How To Define Search View In Odoo

add serarch tag in guest_view.xml

```xml
<record id="view_hotel_guest_search" model="ir.ui.view">
            <field name="model">hotel.guest.search</field>
            <field name="model">hotel.guest</field>
            <field name="arch" type="xml">
                <search>
                    <field name = "name" string="Guest Name" filter_domain="['|',('name','ilike',self),('age','ilike',self),('code','ilike',self)]"/>
                    <field name = "code"/>
                    <field name = "age"/>
                    <field name = "gender"/>
                </search>
            </field>
    </record>
```

- search view က search bar မှာ ရှာလို့ရအောင် လုပ်ပေးတယ်
- ရှာစေချင်တဲ့ attribute တွေကို search tag ထဲမှာ ထည့်ပေးရုံပဲ့

if you want to search multiple search attribute 
just add **`filter domain`**  code like this 

```xml
<field name = "name" string="Guest Name" filter_domain="['|',('name','ilike',self),('age','ilike',self),('code','ilike',self)]"/>
```






