# Django Models

### Models


* Django web applications access and manage data through Python objects 
referred to as models.


 *Models define the structure of stored data, including the field types 
 and possibly also their maximum size, default values, selection list 
 options, help text for documentation, label text for forms, etc.

* The definition of the model is independent of the underlying database — 
you can choose one of several as part of your project settings.


* Models are usually defined in an application's models.py file. They are 
implemented as subclasses of django.db.models.Model, and can include 
fields, methods and metadata. The code fragment below shows a "typical" 
model, named MyModelName:



`from django.db import models

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta: 
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the url to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])
    
    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name
`

#### Field Types

1- CharField

2- TextField

3- IntegerField

4-DateField and DateTimeField are used for storing/representing dates and 
date/time information (as Python datetime.date in and datetime.datetime 
objects, respectively)


5- EmailField

6- FileField and ImageField

7- AutoField

7- ForeignKey

8- ManyToManyField

9- Metadata

One of the most useful features of this metadata is to control the default ordering of records returned when you query the model type.
