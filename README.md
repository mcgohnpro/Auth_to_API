# Auth to API

## Регистрация нового пользователя

POST запрос по URI https://blog.kata.academy/api/users

**Request**:

headers: Content-Type:application/json 

**body**: 

```JSON
	{
		"user": 
			{
			"username": "kataUserTest",
			"email": "mcgohnpro@gmail.com",
			"password": "password"
			}
	}
```

**Response**:

```JSON
{
"user": {
	"username": "katausertest",
	"email": "mcgohnpro@gmail.com",
	"token": "Здесь токен"
}
}
```

## Аутентификация пользователя

POST запрос по URI https://blog.kata.academy/api/users/login

**Request**:

headers: Content-Type:application/json 

**body**: 
```JSON
{
"user": {
	"email": "mcgohnpro@gmail.com",
	"password": "password"
}
}
```

**Response**:

```JSON
{
"user": {
	"username": "katausertest",
	"email": "mcgohnpro@gmail.com",
	"token": "Здесь токен"
}
}

```

## Получение данных текущего пользователя 

GET запрос по URI https://blog.kata.academy/api/user

**Request**

headers: 
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR51ODc0ODE4LCJpYXQiOjE3MTA2OTA4MTh9.eU8-IEkqqbrFjF8vKkHmtslx72FxkKX5xMvKEbZ6osc

**Response**

```JSON
{
"user": {
	"username": "katausertest",
	"email": "mcgohnpro@gmail.com",
	"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY1ZjcxMjAxOGM4MjhkMWIwMDM5NTliYiIsInVzZXJuYW1lIjoia2F0YXVDc2NzQzLCJpYXQiOjE3MTA2OTI3NDN9.3Ahv_5sHRIgDJIF1YR9-rP7IgChL6xO_7jiC9VEgJa0"
}
}
```

