# Permissions

  - Authentication or identification by itself is not usually sufficient to gain access to information or code.
  - For that, the entity requesting access must have authorization.
  - Together with authentication and throttling, permissions determine whether a request should be granted or denied access.
  - The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user.
  - This corresponds to the IsAuthenticated class in REST framework.
  - A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. 
  - This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.
  
  - __How permissions are determined__:
    - Permissions in REST framework are always defined as a list of permission classes.
    - Before running the main body of the view each permission in the list is checked.
    - If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.
    - When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

