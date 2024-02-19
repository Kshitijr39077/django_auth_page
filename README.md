# django-auth-page

I created this authentication page using JWT tokens authentication. 
Database used is MYSQL

-MYSQL
-MYSQL WOKRBENCH
-POSTMAN

Flow Daigram of the Authentication page:

                /register/ 
                       |
                       v
              [POST with user data]
                       |
                       v
                  RegisterView
                       |
                       v
              [Response with user data]
                       |
                       v
             Client-side Handling 
           
                       |
                       v
                [User registered]


                    /login/ 
                       |
                       v
          [POST with email & password]
                       |
                       v
                  LoginView
                       |
                       v
           [Response with JWT token]
                       |
                       v
             Client-side Cookie Storage

                       |
                       v
               [User authenticated]


                     /user/  
                       |
                       v
                [GET request]
                       |
                       v
                   UserView
                       |
                       v
         [Response with user data or error]
                       |
                       v
              Client-side Handling 
                       |
                       v
              [Display user data or error]


                   /logout/ 
                       |
                       v
              [POST logout request]
                       |
                       v
                Logout View
                       |
                       v
            [Clear cookie & Logout]
                       |
                       v
             
                 Client-side Handling    

                       |
                       v
               [User logged out]
