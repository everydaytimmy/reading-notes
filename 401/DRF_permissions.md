### DRF Permissions

https://www.django-rest-framework.org/api-guide/permissions/

Permissions in REST framework are always defined as a list of permission classes.

The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.
```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
If not specified, this setting defaults to allowing unrestricted access:

'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

You can also set the authentication policy on a per-view, or per-viewset basis, using the APIView class-based views.

```
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```

