# Django REST Framework

## Permissions :

- **Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.**

- **Together with authentication and throttling, permissions determine whether a request should be granted or denied access.**

- **Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.**

### How permissions are determined ?

- **Permissions in REST framework are always defined as a list of permission classes.**

- **Before running the main body of the view each permission in the list is checked.**

### according to the following rules of Permissions :

- **The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.**

- **The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.**

- **The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.**

### Object level permissions

- **REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.**

- **Object level permissions are run by REST framework's generic views when .get_object() is called**

- **This will either raise a PermissionDenied or NotAuthenticated exception, or simply return if the view has the appropriate permissions.**

>>
    def get_object(self):
    obj = get_object_or_404(self.get_queryset(), pk=self.kwargs["pk"])
    self.check_object_permissions(self.request, obj)
    return obj


### Setting the permission policy

**The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting.**

>> 
    REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
    }
>> 
    'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
    ]


**Note: when you set new permission classes via the class attribute or decorators you're telling the view to ignore the default list set in the settings.py file.**


### API Reference

1- **AllowAny**

**The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.**

2- **IsAuthenticated**

**The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.**

**This permission is suitable if you want your API to only be accessible to registered users.**

3- **IsAdminUser**

**The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.**

**This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.**

4- **IsAuthenticatedOrReadOnly**

**The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.**

**This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.**

###  Packages

**DRF -Access Policy**

**Composed Permissions**

**REST Condition**

**DRY Rest Permissions**

**Django Rest Framework Roles**

**Django REST Framework API Key**

**Django Rest Framework Role Filters**

**Django Rest Framework PSQ**