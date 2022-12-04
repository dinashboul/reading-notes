 # Django Tutorial : Working with forms

 **An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server.**

 ##  Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including 

 - text boxes 
 - checkboxes
 - radio buttons
 - date pickers 

 **The form is defined in HTML as a collection of elements inside <form>…</form> tags, containing at least one input element of type="submit".**

 - The field's **type** attribute defines what sort of widget will be displayed. 
 - The **name and id**of the field are used to identify the field in JavaScript/CSS/HTML, 
 -  **value** defines the initial value for the field when it is first displayed.
 - matching team **label** is specified using the label tag (see "Enter name" above), with a for field containing the **id** value of the associated **input**.
 -The **submit** input will be displayed as a button by default


### The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

- **action**: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.

- **method**: The HTTP method used to send the data: post or get.

>> The **POST** method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.

>> The **GET** method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.

### Django form handling process

**Django's form handling for displaying information about our models.**

**A process flowchart of how Django handles form requests is shown below, starting with a request for a page containing a form (shown in green).**


![image](./form_handling_-_standard.png)

1- Display the default form the first time it is requested by the user.
   -The form may contain blank fields if you're creating a new record, or it may be pre-populated with initial values (for example, if you are changing a record, or have useful default initial values).

   -The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).

2- Receive data from a submit request and bind it to the form.

   - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.

3- Clean and validate the data.

   - Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.

   - Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)

4- If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

5- If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).

6- Once all actions are complete, redirect the user to another page.

### Form

**The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields.**

### Declaring a Form

**The declaration syntax for a Form is very similar to that for declaring a Model, and shares the same field types (and some similar parameters).**

>> from django import forms

    class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")


## Form fields

**a single DateField for entering the renewal date that will render in HTML with a blank value, the default label "Renewal date:", and some helpful usage text: "Enter a date between now and 4 weeks (default 3 weeks)."**

## Validation

**Django provides numerous places where you can validate your data. The easiest way to validate a single field is to override the method clean_<fieldname>() for the field you want to check.**

### URL configuration

**Before we create our view, let's add a URL configuration for the renew-books page. Copy the following configuration to the bottom of locallibrary/catalog/urls.py:**

>>
 urlpatterns += [
    path('book/<uuid:pk>/renew/', views.renew_book_librarian, name='renew-book-librarian'),
 ]

### View

**For forms that use a POST request to submit information to the server, the most common pattern is for the view to test against the POST request type (if request.method == 'POST':) to identify form validation requests and GET (using an else condition) to identify the initial form creation request.**

### The template

**Create the template referenced in the view**

- First, we declare the form tags

- specifying where the form is to be submitted (action) and the method for submitting the data (in this case an "HTTP POST") 

- if you recall the HTML Forms overview at the top of the page, an empty action as shown, means that the form data will be posted back to the current URL of the page (which is what we want).

- Inside the tags, we define the submit input, which a user can press to submit the data. 

### Other ways of using form template variable

**Using {{ form.as_table }} as shown above, each field is rendered as a table row. You can also render each field as a list item (using {{ form.as_ul }}) or as a paragraph (using {{ form.as_p }}).**

