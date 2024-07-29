# How To Add Chatter To Form View

go to __manifest__.py
- add `'depends': ['mail'],`

go to guest_view.py
- add
```xml
<form>
	<sheet>
	</sheet>
	 <!--chatter-->
	<div class="oe_chatter">
		<field name="message_follower_ids" group="base.group_user"/>
		<field name="activity_ids"/>
		<field name="message_ids"/>
	</div>
</form>
```

go to guest.py
add
```python
_inherit = ["mail.thread",'mail.activity.mixin']
```

------------

# How To Enable Tracking For Fields

not working for me

------------


# How To Add Search Panel
go to guest_view.xml
add 
```xml
<search>
  <searchpanel>
  	<field name="gender" icon="fa-users" select="multi" enable_counters="1"/>
  </searchpanel>
</search>

```
in the `<search>` tag


------------

# How To Add Many2one Field

resource ပြန်စုရဦးမယ်

# How To Add Date And Datetime Fields

add  appointment.py
```python
appointment_time = fields.Datetime(string='Appointment Time')
booking_date = fields.Datetime(string='Booking Date')
```

add appointment_view.xml
```xml
<tree>
		<field name="guest_id"/>
		<field name="appointment_time"/>
		<field name="booking_date"/>
</tree>
```
add appointment_view.xml in form tag
```xml
<group>
		<field name="guest_id"/>
		<field name="appointment_time"/>
		<field name="booking_date"/>
</group>
```

To view time with  am pm
- go to settings\translation\languages
- add time format `%p`

------------


# How To Set Default Values For Fields

just add appointment.py(Models file)

```python
appointment_time = fields.Datetime(string='Appointment Time', default=fields.Datetime.now)
```
this is time default values `default=fields.Datetime.now`

if you can add `default='male'`

------------



