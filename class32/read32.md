# Permissions

Permissions are used to grant or deny access for different classes of users to different parts of the API. They are run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties.



## How permissions are determined

View ermissions in REST framework are always defined as a list of permission classes. If any permission check fails, an exceptions. PermissionDenied or exceptions. NotAuthenticated exception will be raised. The main body of the view will be affected and the view won't run.



