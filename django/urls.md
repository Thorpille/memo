# Le fichier users.py

### La syntaxe de base du fichier urlpatterns :
    from monapp import views
    urlpatterns = [
      # path('monlien/', views.mafonction),
      ]

### Pour utiliser un fichier différent pour une des app:
    from django.urls import path, include  


    urlpatterns = [
      path('lien_vers_mon_app/', include('monapp.urls')),
    ]
    
### Pour utiliser des arguments via l'url :
    path('mon_app/<str:string_arg>/<int:int_arg>/', views.ma_fonction)
