# [Django React Purity Dashboard](https://appseed.us/product/django-react-purity-dashboard)

Start your Development with an Innovative Admin Template for **Chakra UI** and **React**. Purity UI Dashboard is built with over 70 frontend individual elements, like buttons, inputs, navbars, navtabs, cards or alerts, giving you the freedom of choosing and combining. All components can take variations in colour, that you can easily modify using Chakra's style props. The product comes with a simple JWT authentication flow: login/register/logout. 

> Features

- Innovative **Chakra UI** Design - Creafted by [Creative-Tim](https://bit.ly/3fKQZaL)
- React, Redux, Redux-persist
- Authentication: JWT Login/Register/Logout
- **Full-stack Ready** using a **Django API Server** (open-source project) - Server Features
  - Django / DRF / SQLite3 - a simple, easy to use backend
  - Authentication with JWT (login, logout, register)
  - Docker, Unitary tests

> Links

- [Django React Purity Dashboard](https://appseed.us/product/django-react-purity-dashboard) - product page
- [Django React Purity Dashboard](https://django-react-purity-dashboard.appseed-srv1.com/authentication/sign-in) - LIVE Demo
* Free Support via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br />

## General Information

The product is built using a `two-tier` pattern where the React frontend is decoupled logically and physically from the API backend. How to use the product: 

- `Compile and start` the **Django API Backend**
  - by default the server starts on port `5000`
- `Compile and start` the **React UI**
  - UI will start on port `3000` and expects a running backend on port `5000`
- `Configuration` (Optional)
  - Change the API port
  - Configure the API port used by the React UI to communicate with the backend 

<br />

## Quick-start in Docker

> Clone/Download the source code

```bash
$ git clone  https://github.com/app-generator/django-react-purity-dashboard.git
```

<br />

> Start the Django API

```bash
$ cd django-api
$ docker-compose pull   # download dependencies 
$ docker-compose build  # local set up
$ docker-compose up     # start the app 
```

At this point, the API should be up & running at `http://localhost:5000`, and we can test the interface using POSTMAN or `curl`.

<br />

> Start the React UI (using another terminal)

```bash
$ cd react-ui
$ docker-compose pull   # download dependencies 
$ docker-compose build  # local set up
$ docker-compose up     # start the app 
```

Once all the above commands are executed, the `React UI` should be visible in the browser. By default, the app redirects the guest users to authenticate. 
After we register a new user and Sign IN, all the private pages become accessible. 

<br />

![React Purity Dashboard - Open-source full-stack product with Django API Backend.](https://user-images.githubusercontent.com/51070104/136687466-1dfeeb6b-d474-45df-879b-0857b27eb615.gif) 

<br >


## Manual build

### Start the Django API 

```bash
$ cd django-api
$ 
$ # Create a virtual environment
$ virtualenv env
$ source env/bin/activate
$
$ # Install modules
$ pip install -r requirements.txt
$
$ # Set Up the Database
$ python manage.py migrate
$ 
$ # Start the API
$ python manage.py runserver
```

<br />

### Compile & start the React UI

```bash
$ cd react-ui
$
$ # Install Modules
$ yarn
$
$ # Start for development (LIVE Reload)
$ yarn start 
```

<br />

### Configuration (Optional)

> Change the port exposed by the Django API

```bash
$ python manage.py runserver 5001
```

Now, the API starts on port `5001`. 

<br />

> Update the API port used by the React Frontend

**API Server URL** - `src/config/constant.js` 

```javascript
const config = {
    ...
    API_SERVER: 'http://localhost:5000/api/'  // <-- The magic line
};
```

<br />

## API

For a fast set up, use this POSTMAN file: [api_sample](https://github.com/app-generator/api-server-nodejs-pro/blob/master/media/api.postman_collection.json)

> **Register** - `api/users/register` (**POST** request)

```
POST api/users/register
Content-Type: application/json

{
    "username":"test",
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Login** - `api/users/login` (**POST** request)

```
POST /api/users/login
Content-Type: application/json

{
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Logout** - `api/users/logout` (**POST** request)

```
POST api/users/logout
Content-Type: application/json
authorization: JWT_TOKEN (returned by Login request)

{
    "token":"JWT_TOKEN"
}
```

<br />

## Product UI

> React Flask Authentication - Login 

![React Flask Authentication - Login.](https://user-images.githubusercontent.com/51070104/141444378-763ca3fb-c18c-4558-9730-b42a341a7b22.jpg)

<br />

> React Flask Authentication - Icons

![React Flask Authentication - Icons.](https://user-images.githubusercontent.com/51070104/141444472-8c966396-69dc-46c3-835e-b64329fdbf7d.jpg)

<br />

> React Flask Authentication - Colors

![React Flask Authentication - Colors.](https://user-images.githubusercontent.com/51070104/141444532-46a3bcd0-841b-4725-aa82-122569cd678a.jpg)

<br />

## Links & Resources

- Ask for [Support](https://appseed.us/support) on [Discord](https://discord.gg/fZC6hup)
- See for [React Starters](https://appseed.us/apps/react) - index provided by AppSeed

<br />

---
**[React Flask Authentication](https://blog.appseed.us/react-flask-authentication/)** - Open-source full-stack seed project provided by **AppSeed [App Generator](https://appseed.us/)**
