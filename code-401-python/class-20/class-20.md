# Django Tutorial Part 3: Using models

##   Models: Django web applications access and manage data through Python objects.

###  Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms

## Designing the LocalLibrary models

**When designing your models, it makes sense to have separate models for every "object" (a group of related information)**

## Model primer

**This section provides a brief overview of how a model is defined and some of the more important fields and field arguments.**

- Models are usually defined in an application's models.py file

- **A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables**

### Metadata
**You can declare model-level metadata for your Model by declaring class Meta**

### Methods

**in every model you should define the standard Python class method __str__() to return a human-readable string for each object.**

## Django Tutorial : Django admin site

### The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records

### Advanced configuration

- Each model has a list of individual records, identified by the string created with the model's __str__() method, and linked to detail views/forms for editing. By default, this view has an action menu at the top that you can use to perform bulk delete operations on records.

- The model detail record forms for editing and adding records contain all the fields in the model, laid out vertically in their declaration order.


