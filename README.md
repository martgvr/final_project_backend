# Sobre el proyecto final

Este proyecto final ha sido creado para el curso de Backend de Coderhouse, utilizando las siguiente teconologías:

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101)![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)![Railway](https://img.shields.io/badge/Railway-131415?style=for-the-badge&logo=railway&logoColor=white)

# Características del proyecto

- Vistas generadas desde el servidor utilizando EJS.
- Sistema de registro, login.
- Panel de administración de productos, carritos y usuarios.
- Creación automática de usuario administrador al iniciar servidor.
- Encriptado de contraseñas en base de datos utilzando Bcrypt.
- Envío de emails realizado con Nodemailer.

# Panel de administrador

<img src="https://i.ibb.co/1Xjqgs6/panel1.png" alt="Chat">

# Sistema de mensajería

<img src="https://i.ibb.co/64hZ47L/chat.png" alt="Chat">

# Variables de entorno (.env)

```
MONGO_URL = ''
SECRET_KEY = ''

CLUSTER = [true | false]
PORT = 8080
DAO = [mongo | sqlite]

NODEMAILER_USER = ''
NODEMAILER_PASS = ''

ADMIN_USER = ''
ADMIN_PASS = ''
ADMIN_EMAIL = ''
```

# Endpoints

## Products

```
POST
/products

{
  "name": "",
  "price": number,
  "photo": "",
  "category": ""
}

GET
/products
/products/:id

PUT
/products/:id

{
  "name": "",
  "price": number,
  "photo": "",
  "category": ""
}

DELETE
/products/:id

```

## Carts

```
POST
/carts
/carts/checkout

GET
/carts

DELETE
/carts/:id

```

## Orders

```
POST
/orders

{
  "products": "",
  "status": "",
  "timestamp": "",
  "orderEmail": "",
  "orderID": ""
}

GET 
/orders
/orders/:id

PUT
/orders/:id

{
  "products": "",
  "status": "",
  "timestamp": "",
  "orderEmail": "",
  "orderID": ""
}

DELETE
/orders/:id
/orders/all
```

## Users

```
GET
/users/:username

PUT
/users/:username
```