### Docker

https://wsvincent.com/beginners-guide-to-docker/

Docker is really just Linux containers which are a type of virtualization.

Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command sudo pip install docker-compose after your Docker installation is complete.

A good command to inspect Docker is `docker info` which we can run now. It will contain a lot of output but focus on the top lines which show we now have 1 container which is `stopped` and 1 image.

Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.

A baking analogy we can use here is as follows:

A `Dockerfile` is the recipe for a cake
An image is a snapshot of the recipe at a given time
A `docker-compose.yml` says how to make the cake
And the container is the actual, baked cake


### Django REST

https://djangoforapis.com/library-website-and-api/

The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

Django REST Framework is added just like any other third-party app. Make sure to quit the local server Control + c if it is still running. Then on the command line type the below.

`pipenv install djangorestframework~=3.11.0`

Let’s first create a new api app.

`$ python manage.py startapp api`
Then add it to `INSTALLED_APPS.`

#### Serializers
A serializer translates data into a format that is easy to consume over the internet, typically JSON, and is displayed at an API endpoint.

```
# api/serializers.py
from rest_framework import serializers

from books.models import Book


class BookSerializer(serializers.ModelSerializer):
    class Meta:
        model = Book
        fields = ('title', 'subtitle', 'author', 'isbn')
```
     
       

