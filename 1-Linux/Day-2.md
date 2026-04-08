# Day 2: Temporary User Setup with Expiry


## 🐛Task
As part of the temporary assignment to the Nautilus project, a developer named yousuf requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:

Create a user named yousuf on App Server 1 in Stratos Datacenter. Set the expiry date to 2024-01-28, ensuring the user is created in lowercase as per standard protocol.


## 🛠️Solution

```sudo useradd -m -e 2024-01-28 yousuf```

```sudo usermod -e 2024-01-28 yousuf```

```cat /etc/passwd```

```sudo su yousuf```

```chage -l yousuf```

```passwd -S yousuf```

```passwd -l yousuf```

```passwd -u yousuf```

```passwd -d yousuf```


---
