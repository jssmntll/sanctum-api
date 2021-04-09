# Laravel REST API con Sanctum

Ejemplo de una REST API usando tokens de autenticación con Laravel Sanctum

## Uso

Crea un archivo _database.sqlite_ en el directorio _database_ O utiliza una base de datos diferente y agregua su configuración al archivo _.env_

```
# Ejecuta el servidor web en el puerto 8000
php artisan serve
```

## Rutas

```
# Públicas
POST   /api/login
@body: email, password
POST   /api/register
@body: name, email, password, password_confirmation
GET   /api/products
GET   /api/products/:id
GET   /api/search/:string

# Privadas
POST   /api/products
@body: name, slug, description, price
PUT   /api/products/:id
@body: ?name, ?slug, ?description, ?price
DELETE  /api/products/:id
POST    /api/logout
