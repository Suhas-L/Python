# Website Blocker

# Introduction

This application can be used to block the websites so that the user can not open them during the specific period.

# Objective
The objective of Python website blocker is to block some certain websites which can distract the user during the specified amount of time.



In this, we will block the access to the list of some particular websites during the working hours so that the user can only access those websites during the free time only.

The working time in this python application is considered from 9 AM to 5 PM. The time period except that time will be considered as free time.

Process
To block the access to a specific website on the computer, we need to configure the hosts file.

The hosts file
The hosts file is a local file which was used to map hostnames to IP addresses in the old days. Although the DNS service is used nowadays to map the hostnames to the IP addresses, the host file is still very complex and can be used to configure the mapping of the IP addresses locally.

Location of hosts file
The location of the hosts file varies from operating system to operating system.

Windows: C:\Windows\System32\drivers\etc

mac and Linux: /etc/hosts

Configuration
Since the hosts file contains the mapping between the host names and IP addresses, let's look at the content of our hosts file first stored as /etc/hosts as we use CentOS 7 (Linux).


Python Website Blocker
As we can see in the above image, the mappings are saved for the localhost with the IP address 127.0.0.1.

Similarly, we can redirect any hostname back to the localhost IP (127.0.0.1). It will block the access to that hostname and redirect that to localhost on each request.

For testimony, let's edit the content of hosts file and add some of the following lines to it. To make changes to the /etc/hosts file, we will need to change its permissions.

Run the following command on the terminal to change the permissions.

$ sudo chmod 777 /etc/hosts   
Now add the following line to the file to block the access to facebook.com (for example).


127.0.0.1       www.facebook.com   
As shown in the image below.

Python Website Blocker
Save the file and try to open the www.facebook.com using the browser.

Python Website Blocker
As shown in the above figure, it is refused to connect.


We have completed our task by manually editing the hosts file. We haven't achieved our objective yet. Our objective is to block access to some particular websites (for example, facebook) during working hours only (9 AM to 5 PM).

It needs a python script which keeps adding the necessary lines to the hosts file during a particular period.

In this section of the tutorial, we will build such python script which keeps editing the hosts file during the working hours. We will also deploy that script at the OS startup so that it doesn't need any external execution.

# Requirements
We need to know the following python modules to build the python website blocker.

file handling: file handling is used to do the modifications to the hosts file.
time: The time module is used to control the frequency of the modifications to the hosts file.
datetime: The datetime module is used to keep track of the free time and working time.
