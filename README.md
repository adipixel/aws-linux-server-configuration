# Linux server Configuration

#### Server Details
- Service Provider: Amazon Web Service - Lightsail
- Operating System: Ubuntu
- IP address: 13.59.55.238
- SSH port: 2200
- URL: ec2-13-59-55-238.us-east-2.compute.amazonaws.com

### Summary

Deployed a RESTful web application that provides a list of items within a variety of categories as well as provide a user registration and authentication system. Registered users will have the ability to post, edit and delete their own items.



### Server Configurations:
#### User Management
- Cannot log in as root remotely
- A new user - `grader` is created and can user can run commands using sudo to inspect files that are readable only by root

#### Security
Ports allowed by Uncomplicated Firewall for SSH, HTTP and NTP are `2200`, `80` and `123` respectively
`SSH` is hosted on non-default port
Key-based `SSH` authentication is enforced
All system packages have been updated to most recent versions

#### Application Functionality
- The web server responds on port 80
- Database server has been configured to serve data (PostgreSQL)
- Web server has been configured to serve the Item Catalog application as a WSGI app

### Lessons learned
- How to access, secure, and perform the initial configuration of a bare-bones Linux server
- Deployment of web applications to a publicly accessible server
- Properly securing the application ensures that the application remains stable and that the user’s data is safe