# Volunteer-Platform-Sudan 🇸🇩
A PHP-based graduation project that serves as an online volunteering portal in Sudan. It allows volunteers to register, apply for opportunities, and interact with organizations managing community projects.

## Abstract
An online **volunteer portal** designed to connect **volunteers** with **organizations and community initiatives** across Sudan. This application provides the ability for volunteers to create accounts, build profiles, upload resumes, search for volunteer opportunities, and apply to projects.  
Organizations can register, post volunteer opportunities, view applicants, and manage their campaigns.



## 🎯 Key Features
- Volunteer registration and login system
- Profile creation and resume upload
- Search and apply to volunteer projects
- Organization account management
- Posting and managing volunteer opportunities
- Admin panel for system oversight
- Email verification (optional)
- Simple user interface based on PHP & MySQL



## 🎓 Graduation Project Info

This project was developed as part of my **Bachelor's degree final year project** in **Information Technology** at **Nile University**, Sudan (2025).  
Its aim is to **promote social impact and civic engagement** through a digital platform that makes volunteering easier and more accessible across Sudan.

 🔐 All login credentials, emails, and database content are for **testing and demonstration purposes only**.



## 🚀 How to Set Up Locally

1. Create a MySQL database named `volunteers`
2. Import the provided `volunteers.sql` file (contains sample users and organizations)
3. Configure database connection in `db.php`:

```php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "volunteerportal";
```
 ## Volunteer Accountّّّّّّ:
 //Note2: All Password are encrpyted through code so you CANNOT change password directly from database.
 ```
Email: Osmano123@gmail.com
Password: 123456
```
##  Organization Account:
//Note2: All Password are encrpyted through code so you CANNOT change password directly from database.
```
Email: icrc123@gmail.com
Password: 123456
```
## Admin :
//Note: Password is not encrpyted from code so you CAN change directly from database.
```
Username: admin
Password: 123456
```

🛠️ Note: For email confirmation, set `active = 1 `manually in the database for new users if using localhost.


🛠️ Note: If you are testing on real server then you can uncomment the following code from 
`adduser.php`

php
// Send Email
```php
$to = {CANDIDATE_EMAIL ADDRESS};
$subject = "Sudannes Volunteer - Confirm Your Email Address";
$message = '
    <html>
    	 <head>
		    <title>Confirm Your Email</title>
		</head>
		<body>
		    <p>Click Link To Confirm</p>
		    <a href="{YOUR_REAL_DOMAIL}/verify.php?token='.$hash.'&email='.$email.'">Verify Email</a>
		</body>
	</html>
';
$headers[] = 'MIME-VERSION: 1.0';
$headers[] = 'Content-type: text/html; charset=iso-8859-1';
$headers[] = 'To: '.$to;
$headers[] = 'From: hello@yourdomain.com';
// You can add more headers like Cc, Bcc;
$result = mail($to, $subject, $message, implode("\r\n", $headers)); // \r\n will return new line. 
if($result === TRUE) {
//If email sent successfully then Set some session variables and redirect to login page
	$_SESSION['registerCompleted'] = true;
	header("Location: login.php");
	exit();
}
```
🧑‍💻 Technologies Used
- PHP
- MySQL
- HTML/CSS
- Bootstrap
- Git & GitHub

📬 Contact
Feel free to reach out via email: osmanhasspo@gmail.com
Or visit my LinkedIn: LinkedIn Profile

🤝 Contribution & Thanks
Inspired by community needs in Sudan.

UI based on open-source tutorials adapted for volunteer work context.
