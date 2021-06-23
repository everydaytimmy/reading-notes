### Django Forms

https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms

Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed). What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.

A process flowchart of how Django handles form requests is shown below, starting with a request for a page containing a form (shown in green).


![Django forms](https://user-images.githubusercontent.com/45111611/123124130-69d68400-d415-11eb-92ad-baefb281c1b1.png)


```
from django import forms

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")
```

There are a LOT of form fields:

There are many other types of form fields, which you will largely recognize from their similarity to the equivalent model field classes: BooleanField, CharField, ChoiceField, TypedChoiceField, DateField, DateTimeField, DecimalField, DurationField, EmailField, FileField, FilePathField, FloatField, ImageField, IntegerField, GenericIPAddressField, MultipleChoiceField, TypedMultipleChoiceField, NullBooleanField, RegexField, SlugField, TimeField, URLField, UUIDField, ComboField, MultiValueField, SplitDateTimeField, ModelMultipleChoiceField, ModelChoiceField.

The arguments that are common to most fields are listed below (these have sensible default values):

 - required: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.
 - label: The label to use when rendering the field in HTML. If a label is not specified, Django will create one from the field name by capitalizing the first letter and replacing underscores with spaces (e.g. Renewal date).
 - label_suffix: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other character(s).
 - initial: The initial value for the field when the form is displayed.
 - widget: The display widget to use.
help_text (as seen in the example above): Additional text that can be displayed in forms to explain how to use the field.
 - error_messages: A list of error messages for the field. You can override these with your own messages if needed.
 - validators: A list of functions that will be called on the field when it is validated.
 - localize: Enables the localization of form data input (see link for more information).
 - disabled: The field is displayed but its value cannot be edited if this is True. The default is False.
