# Odoo modules

## Requerimientos

- Docker

## Instalación

```bash
# Clonar el repositorio
git clone https://github.com/victorze/odoo-modules.git

# Iniciar un servidor PostgreSQL
docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres -p 5432:5432 --name db postgres:10

# Iniciar una instancia de Odoo
docker run -d -v `pwd`/config:/etc/odoo -v `pwd`/addons:/mnt/extra-addons -p 8069:8069 --name odoo --link db:db -t odoo:14

# Ir a la URL:
127.0.0.1:8069

# Buscar e instalar módulos (por ejemplo el módulo openacademy)
```
