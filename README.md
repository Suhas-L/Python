# Website Blocker

# Introduction

This application can be used to block the websites so that the user can not open them during the specific period.

# Objective
The objective of Python website blocker is to block some certain websites which can distract the user during the specified amount of time.

![intro](https://user-images.githubusercontent.com/80455876/125286340-9cd4af00-e313-11eb-8a72-8199e999bf93.jpg)

In this, we will block the access to the list of some particular websites during the working hours so that the user can only access those websites during the free time only.

The working time in this python application is considered from 9 AM to 5 PM. The time period except that time will be considered as free time.

# Process
To block the access to a specific website on the computer, we need to configure the hosts file.

# The hosts file
The hosts file is a local file which was used to map hostnames to IP addresses in the old days. Although the DNS service is used nowadays to map the hostnames to the IP addresses, the host file is still very complex and can be used to configure the mapping of the IP addresses locally.

# Location of hosts file
The location of the hosts file varies from operating system to operating system.

Windows: C:\Windows\System32\drivers\etc

mac and Linux: /etc/host.


# Requirements
We need to know the following python modules to build the python website blocker.

file handling: file handling is used to do the modifications to the hosts file.

time: The time module is used to control the frequency of the modifications to the hosts file.

datetime: The datetime module is used to keep track of the free time and working time.
