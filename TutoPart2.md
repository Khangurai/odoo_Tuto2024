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







