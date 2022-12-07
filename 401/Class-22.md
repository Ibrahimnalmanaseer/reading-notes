# Django CRUD and Forms

## Form Overview
An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server. Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests with cross-site request forgery protection.

## HTML Forms (Normal Form)

The form is defined in HTML as a collection of elements inside `<form>…</form>` tags, containing at least one input element of type="submit".
```
<form action="/team_name_url/" method="post">
  <label for="team_name">Enter name: </label>
  <input
    id="team_name"
    type="text"
    name="name_field"
    value="Default name for team." />
  <input type="submit" value="OK" />
</form>
```

## Django Form 

 Django handles form requests as shown below,starting with a request for a page containing a form (shown in green).
 

![form_handling_-_standard](https://user-images.githubusercontent.com/62019258/205456085-35159d95-e6d3-4b47-b2c8-ac86339693d7.png)

The most fundamental is the `Form` class, which simplifies both generation of form HTML and data cleaning/validation


### Form 

The `Form` class is the heart of Django's form handling system. It specifies the fields in the `form`.

```
from django import forms
 
# creating a form
class InputForm(forms.Form):
 
    first_name = forms.CharField(max_length = 200)
    last_name = forms.CharField(max_length = 200)
    roll_number = forms.IntegerField(
                     help_text = "Enter 6 digit roll number"
                     )
    password = forms.CharField(widget = forms.PasswordInput())
```



### Render form into a view

```
from django.shortcuts import render
from .forms import InputForm
 

def home_view(request):
    context ={}
    context['form']= InputForm()
    return render(request, "home.html", context)


```

### Edit templates > home.html


```

<form action = "" method = "post">
	
	{{form }}
	<input type="submit" value=Submit">
</form>

```

