# Weather App

A copy of the assessment requirements can be found [here](https://docs.google.com/document/d/1DbHY7J1huLH1dKuRE9K5KBglb2x2ZwGL7lL4I91WyIk/edit?usp=sharing)

## Local setup instructions

- Run the command below to get the backend and frontend submodules.

  ```bash
  git clone --recurse-submodules https://github.com/mirror83/weather-app
  ```

### Backend setup

- Navigate to the backend repository and install PHP dependencies with Composer:
  ```bash
  cd weather-app-backend
  composer install
  ```
- Copy the example environment file and generate an application key:
  ```bash
  cp .env.example .env
  php artisan key:generate
  ```
- [Sign up](https://openweathermap.org/api) for an OpenWeatherMap API key.
- Add the API key to the `.env` file in the backend repository.
- Run the server with
  ```bash
  php artisan serve
  ```
  The api should be accessible on `localhost:8000/api`

### Frontend setup

- Install dependencies with
  ```bash
  npm install
  ```
- Copy the example environment file:
  ```bash
  cp .env.example .env
  ```
- Set the env variable `NEXT_PUBLIC_API_URL` to the backend API URL
- Run the dev server with:
  ```bash
  npm run dev
  ```
