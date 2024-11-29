# secure-file-sharing
A secure file-sharing application built using Django and Python that supports user authentication, file uploads, and secure file downloads. The application implements token-based authentication for added security and provides distinct functionalities for different user roles (e.g., Ops users and Client users).

# Features
#### User Authentication: Signup, login, and token-based authentication using Django's built-in authentication system.
#### Role-based Access Control:
#### Ops Users: Can upload files.
#### Client Users: Can list and download files.
#### File Upload and Download: Securely upload files (Ops users) and download them (Client users).
#### Token Authentication: Secure access to API endpoints using tokens.


# Installation
## Prerequisites
 Ensure you have the following installed:

#### Python (>= 3.6)
#### pip (Python package manager)
#### Git

# Steps
 ### Clone the Repository:
       ``` 
            git clone https://github.com/gaurharsh/secure-file-sharing.git
            cd secure-file-sharing
      ` ` ` 

 ### Create a Virtual Environment:
       ` ` `
            python -m venv venv
           source venv/bin/activate  # On Windows: venv\Scripts\activate
      ` ` `

### Install Dependencies:
           ` ` ` 
            pip install -r requirements.txt
            
           ` ` `
             

 ###  Apply Migrations:
       ` ` ` 
        python manage.py makemigrations
        python manage.py migrate
      ` `  `

### Create a Superuser (Admin Account):
    ` ` `
       python manage.py createsuperuser
  ` ` ` 

### Run the Development Server:

 ` ` ` 
       python manage.py runserver
 ` ` ` 

###   Access the Application:

` ` ` 
     Visit http://127.0.0.1:8000/ in your browser.
` ` ` 
