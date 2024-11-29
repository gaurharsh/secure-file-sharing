## secure-file-sharing
A secure file-sharing application built using Django and Python that supports user authentication, file uploads, and secure file downloads. The application implements token-based authentication for added security and provides distinct functionalities for different user roles (e.g., Ops users and Client users).

## Features
#### User Authentication: Signup, login, and token-based authentication using Django's built-in authentication system.
#### Role-based Access Control:
#### Ops Users: Can upload files.
#### Client Users: Can list and download files.
#### File Upload and Download: Securely upload files (Ops users) and download them (Client users).
#### Token Authentication: Secure access to API endpoints using tokens.


## Installation
###  Prerequisites
 Ensure you have the following installed:

#### Python (>= 3.6)
#### pip (Python package manager)
#### Git

## Steps
 #### Clone the Repository:
       ``` 
            git clone https://github.com/gaurharsh/secure-file-sharing.git
            cd secure-file-sharing
      ` ` ` 

 #### Create a Virtual Environment:
       ` ` `
            python -m venv venv
            source venv/bin/activate  # On Windows: venv\Scripts\activate
      ` ` `

#### Install Dependencies:
           ` ` ` 
                 pip install -r requirements.txt
            
           ` ` `
             

 ####  Apply Migrations:
       ` ` ` 
           python manage.py makemigrations
           python manage.py migrate
       
      ` `  `

#### Create a Superuser (Admin Account):
      ` ` `
            python manage.py createsuperuser
        
      ` ` ` 

### Run the Development Server:
 
   ` ` ` 
           python manage.py runserver
           
   ` ` ` 

####   Access the Application:

 
         Visit http://127.0.0.1:8000/ in your browser.
         
  


 #### API Endpoints

 ##### 1. User Signup (POST /signup/)
 
          URL:  http://127.0.0.1:8000/signup/ 
      
 
 

#####  Payload Example (JSON):
 
     ` ` ` 
          {
              "username": "testuser",
             "password": "password123"
          }
          
    ` ` ` 

##### 2. User Login (POST /login/)
       
                URL:  http://127.0.0.1:8000/login/
   
      


##### Payload Example (JSON):
       ` ` `
                    {
                      "username": "testuser",
                     "password": "password123"
                    }
 
         ` ` `

 ##### Response:
       ` ` `
                  {
                 "token": "your_generated_token"
                  }

       ` ` ` 

##### 3. File Upload (POST /upload/) [Ops User Only]

   
        URL:  http://127.0.0.1:8000/upload/ 
 


##### Headers:

 ` ` ` 
        Authorization: Token <your_token>
 ` ` `  

#### Value: Choose the file to upload.

#####  4. List Files (GET /files/) [Client User Only]

  
       URL: http://127.0.0.1:8000/files/ 
  


#### Headers:

     ` ` ` 
         Authorization: Token <your_token>
    ` ` ` 


##### 5. Download File (GET /files/<file_id>/download/) [Client User Only]
  
           URL: http://127.0.0.1:8000/files/<file_id>/download/


#### Headers:

      ` ` `
             Authorization: Token <your_token>
      ` ` `

###  Project Structure
secure-file-sharing/
│
├── files/                   # Django app for handling file upload/download
│   ├── migrations/          # Database migrations
│   ├── models.py            # Database models
│   ├── views.py             # API views
│   ├── urls.py              # App-specific URL configurations
│   └── ...
│
├── secure_file_sharing/     # Main project folder
│   ├── settings.py          # Project settings
│   ├── urls.py              # Project URL configurations
│   └── ...
│
├── manage.py                # Django management script
└── requirements.txt         # Python dependencies




#### Author
 ##### Harshvardhan 
