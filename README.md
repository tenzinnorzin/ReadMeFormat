<!-- Improved compatibility of back to top link -->
<a id="readme-top"></a>

<!-- PROJECT LOGO --> 
<br /> 
<div align="center"> <h1 align="center">HyphenView</h1> 
<p align="center"> A modern React-based web application for data visualization and management. 
<br /> 
</div> 
<!-- TABLE OF CONTENTS --> 

<details> <summary>Table of Contents</summary> 
  <ol> 
    <li> <a href="#about-the-project">About The Project</a> 
      <ul> <li><a href="#built-with">Built With</a></li> </ul> 
    </li> 
    <li> <a href="#getting-started">Getting Started</a> 
      <ul> 
      <li><a href="#prerequisites">Prerequisites</a></li> 
      <li><a href="#installation">Installation</a></li> 
      </ul> </li> <li><a href="#usage">Usage</a></li> 
    <li><a href="#contributing">Contributing</a></li> 
    <li><a href="#license">License</a></li> 
    <li><a href="#contact">Contact</a></li> 
  </ol> 
</details> 
<!-- ABOUT THE PROJECT -->

# About The Project
HyphenView is a modern React-based web application designed to provide robust and efficient data visualization and management. This project leverages React, Python APIs, MySQL, and Node.js to deliver an integrated user experience. This repository contains the source code and deployment instructions for setting up HyphenView on an Ubuntu server.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Built With
* React 18
* Python 3.11
* MySQL
  
<p align="right">(<a href="#readme-top">back to top</a>)</p> 

<!-- GETTING STARTED -->

# Getting Started
Follow these steps to set up and deploy HyphenView on your local or production environment.

## Prerequisites
Ensure you have the following installed:

* Ubuntu 20.04 or higher
* Python 3.12.4
* MySQL Server
* Node.js (v20.5.0)
* NPM (via Node.js)
* NVM (Node Version Manager)

<p align="right">(<a href="#readme-top">back to top</a>)</p> 

## Installation
### 1. Clone the Repository

```sh
  git clone <repository_url>
  cd HyphenView
  ```

### 2. Python Environment Setup

Install Python and pip:
```sh
sudo apt install -y python3.11 python3-pip
```

Install project dependencies:
```sh
pip3 install -r requirements.txt
```

### 3. Database Setup

Install MySQL server and client:
```sh
sudo apt install -y mysql-server mysql-client
```

Import the database schema:
```sh
mysql -u root -p hyphenview_schema < /path/to/hyphenview_dump.sql
```

### 4. Node.js and React Setup

Install NVM:
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
source ~/.nvm/nvm.sh
```

Install Node.js and npm:
```sh
nvm install 20.5.0
nvm use 20.5.0
```

Navigate to the React application directory:
```sh
cd HyphenView/HyphenView
```

Update .env with the machine’s IP:
```sh
REACT_APP_API_URL=http://<your_machine_ip>:8000
```

Start the React application:
```sh
npm start
```

### 5. Start Python APIs

Navigate to the Python API directory:
```sh
cd HyphenView/Hyphen_api/app
```

Run the main API file:
```sh
python main.py
```

The APIs will start, and you will see logs similar to this:
```sh
INFO:     Uvicorn running on http://0.0.0.0:8000 (Press CTRL+C to quit)
```

<p align="right">(<a href="#readme-top">back to top</a>)</p> 
