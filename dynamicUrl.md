### Dynamic Url

 1-urls.py

```python
from django.urls import path
from . import views

urlpatterns = [
 
    path('<str:pk>', views.show, name='show'),
```

> we create a path to receive a string form the user 



2-views.py 

```python
def show (request,pk):
	return HttpResponse(f'the word on url is <strong> {pk}>')
```

> we create a view to take the pk *(you can change the name )*  from url path and return it in Http resopnse 
