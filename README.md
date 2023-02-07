# Reset-your-forgotten-superuser-password-in-Django

 python manage.py shell
 from django.contrib.auth import get_user_model 
 print(get_user_model().objects.filter(is_superuser=True).values_list('username',flat=True))
 user=get_user_model().objects.get(username='User_Name') 
 user.set_password('SecreatPassword')
 user.save()
