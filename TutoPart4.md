
# Understanding Rec Name

note ကျန်

------------

# How To Add Notebook And Pages
note ကျန်

------------
# How To Define HTML Field

add appointment.py
`room = fields.Html(string='Room')`
```xml
<notebook>
	<page string="Room" name="Room">
	<field name="room" placeholder="Enter your room"/>
	</page>
	<page string="Services" name="Services">
	</page>
</notebook>
```
---------------

# Remove Create, Edit, Delete and Duplicate Options From Views 

ကိုယ်ပေးမလုပ်ချင်တဲ့ model ,form တွေကို zero ပေးရင် permission ပိတ်တာနဲ့တူတူပဲ့
`<form></form>` `<tree></tree>`

> create="0" delete="0" edit="0"

```xml
<form create="0" delete="0" edit="0">
</form>
<tree create="0" delete="0" edit="0">
</tree>
```

------------
# Working Of Priority Widget

star widget ထည့်နည်း

add code to appointment.py
```xml
priority = fields.Selection([
        ('0', 'Very Low'),
        ('1', 'Low'),
        ('2', 'Normal'),
        ('3', 'High')], string='Priority')
```
add xml format to view
```xml
<form>
	<sheet>
		<div class="oe_title">
			<h2>
				<field name="priority" widget="priority" class="mr-3"/>
			</h2>
		</div>
```

------------

# How To Add Buttons

## Show Confirmation Message On Button Click

# How To Add Help Messages For Fields And Buttons

# How To Fix Compute Method Failed To Assign Value Error

# Rainbow Effect

# Badge Widget And Decorations

# How To Give Color For Tree View Records

# Widget List Activity In Odoo

# Dynamic Tree View

# Many2one Avatar And Many2One Avatar User Widget 

add field in appointment.py not working

# odoo module auto update command

go to pycharm \edit configuration\ type `-c conf/odoo.conf -u hotel_B`

#






