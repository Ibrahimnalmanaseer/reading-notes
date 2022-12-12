# Django Permissions

## Permission

Permissions are used to grant or deny access for different classes of users to different parts of the API.

## How permissions are determined

Permissions in REST framework are always defined as a list of permission classes.

Before running the main body of the view each permission in the list is checked. If any permission check fails, an `exceptions.PermissionDenied` or `exceptions.NotAuthenticated` exception will be raised, and the main body of the view will not run.

## Object level permissions

Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

we need to explicitly call the `.check_object_permissions(request, obj)` method on the view at the point at which you've retrieved the object.

This will either raise a `PermissionDenied` or `NotAuthenticated` exception, or simply return if the view has the appropriate permissions.

