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

[![devide view form](2 "devide view form")](https://github.com/Khangurai/odoo_Tuto2024/blob/main/assests/2.png "devide view form")

>**to devide the form group like this** 

**add code in this section between `<group>` tag** 

```xml
<form>
                    <sheet>
                        <group><group>
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

