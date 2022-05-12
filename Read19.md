# Django Forms

Working with forms can be complicated! Developers need to write HTML for the form, validate and properly sanitize entered data on the server (and possibly also in the browser), repost the form with error messages to inform users of any invalid fields, handle the data when it has successfully been submitted, and finally respond to the user in some way to indicate success. **Django Forms take a lot of the work out of all these steps, by providing a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction**..

create form by regular way by creating the HTML, validating the returned data, re-displaying the entered data with error reports if needed, and performing the desired operation on valid data can all take quite a lot of effort to "get right". Django makes this a lot easier by taking away some of the heavy lifting and repetitive code!

## Django form handling process

The main things that Django's form handling does are:

1 - Display the default form the first time it is requested by the user.

- The form may contain blank fields if you're creating a new record, or it may be pre-populated with initial values (for example, if you are changing a record, or have useful default initial values).

- The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).

2 - Receive data from a submit request and bind it to the form.

- Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.

3 - Clean and validate the data.

- Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.

- Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)

4 - If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

5 - If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).

6 - Once all actions are complete, redirect the user to another page.

## ModelForms

if you just need a form to map the fields of a single model then your model will already define most of the information that you need in your form: fields, labels, help text and so on. Rather than recreating the model definitions in your form, it is easier to use the ModelForm helper class to create the form from your model. This ModelForm can then be used within your views in exactly the same way as an ordinary Form.

A basic ModelForm containing the same field as our original RenewBookForm is shown below. All you need to do to create the form is add class Meta with the associated model (BookInstance) and a list of the model fields to include in the form.

    from django.forms import ModelForm

    from catalog.models import BookInstance

    class RenewBookModelForm(ModelForm):
        class Meta:
            model = BookInstance
            fields = ['due_back']

The rest of the information comes from the model field definitions (e.g. labels, widgets, help text, error messages). If these aren't quite right, then we can override them in our class Meta, specifying a dictionary containing the field to change and its new value. For example, in this form, we might want a label for our field of "Renewal date" (rather than the default based on the field name: Due Back), and we also want our help text to be specific to this use case. The Meta below shows you how to override these fields, and you can similarly set widgets and error_messages if the defaults aren't sufficient. 

    class Meta:
        model = BookInstance
        fields = ['due_back']
        labels = {'due_back': _('New renewal date')}
        help_texts = {'due_back': _('Enter a date between now and 4 weeks (default 3).')}
