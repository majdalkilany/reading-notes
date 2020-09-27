## Permissions 

Authentication or identification by itself is not usually sufficient to 
gain access to information or code. For that, the entity requesting 
access must have authorization.

**Permissions are used to grant or deny access for different classes of users to different parts of the API.**

The simplest style of permission would be to allow access to any 
authenticated user, and deny access to any unauthenticated user. This 
corresponds to the IsAuthenticated class in REST framework.

### How permissions are determined  

* Permissions in REST framework are always defined as a list of permission classes 

###### When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

* The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.

* The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.


* The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.


### Object level permissions

Object level permissions are run by REST framework's generic views when .
get_object() is called. As with view level permissions, an exceptions.
PermissionDenied exception will be raised if the user is not allowed to 
act on the given object

If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.


#### Setting the permission policy


The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.

`REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}`


### API Reference

##### API Reference

The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

This permission is not strictly required, since you can achieve the same 
result by using an empty list or tuple for the permissions setting, but 
you may find it useful to specify this class because it makes the 
intention explicit.

#### IsAuthenticated 

The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

This permission is suitable if you want your API to only be accessible 
to registered users.


#### IsAdminUser
The IsAdminUser permission class will deny permission to any user, 
unless user.is_staff is True in which case permission will be allowed.


This permission is suitable if you want your API to only be accessible 
to a subset of trusted administrators.

#### IsAuthenticatedOrReadOnly

The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request.





 Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.

