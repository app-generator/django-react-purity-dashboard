# Change Log

## [1.0.4] 2022-11-05
### Improvements

- Updated for Deploy on RENDER using [Python Deployer](https://github.com/app-generator/deploy-automation-render)
  - `python.exe .\deployer.py django https://github.com/app-generator/api-server-django`
  - The new API is usable via `https://api-server-django-<RANDOM>.onrender.com/api/`

## [1.0.3] 2022-10-03
### Improvements

- Fix Docker Scripts

## [1.0.2] 2022-06-07
### Improvements

- Update Docker Scripts
  - App served now by Gunicorn
- Update Dependencies

## [1.0.1] 2022-01-28
### Improvements

- Dependencies update (all packages) 
  - `Django==4.0.1`

## [1.0.0] 2021-07-20
### First stable version

> Features: 

- API:
   - Sign UP: `/api/users/register`
   - Sign IN: `/api/users/login`
   - Logout: `/api/users/logout`
   - Check Session: `/api/users/checkSession`
   - Edit User: `/api/users/edit`
- Docker
