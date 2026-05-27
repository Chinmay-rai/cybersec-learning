# Day 27 – Linux Package Management and Password Management

## What I Did
- Studied Linux package management concepts  
- Learned how the `dpkg` command works at the lowest level for package management in Debian-based systems  
- Studied how `apt-get` acts as a front-end tool for `dpkg` and simplifies package management  

- Learned package management commands such as:
  - `apt-get update`
  - `apt-cache search`
  - `apt-get install`
  - `apt-get upgrade`

- Studied how package installation and updating works:
  - Installing packages using `apt-get install`
  - Updating already installed packages
  - Updating all system packages using:
    - `apt-get update`
    - `apt-get upgrade`

- Studied package removal methods:
  - `apt-get remove`
  - `apt-get purge`

- Learned the difference between removing packages normally and completely removing configuration files  

- Studied Linux password management using the `passwd` command  
- Learned:
  - How users can change their passwords
  - Root user privileges related to password management
  - Viewing password status information using the `-S` option  

## What I Understood
- Linux package managers simplify software installation, updating, and removal  
- `apt-get` provides an easier interface for working with low-level package tools like `dpkg`  
- Updating package lists before installation is an important system management practice  
- Different package removal methods affect whether configuration files remain on the system  
- Linux provides built-in tools for secure password and user management  

## Concepts Covered
- `dpkg`
- `apt-get`
- `apt-cache`
- Package installation
- Package upgrades
- Package removal
- `remove` vs `purge`
- `passwd` command
- Password status information

## Key Takeaways
- Package management is one of the most important parts of Linux system administration  
- Linux package managers automate software handling and dependency management  
- Understanding package management is useful for Linux administration and cybersecurity environments  
- User and password management are important system security concepts  

## Next Step
- Continue learning Linux system administration and process-related concepts
