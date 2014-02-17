# Vagrant Ansible Python
Creates a very basic Ansible-provisioned Vagrant development server, for use with Python projects.

- Updates the `apt` cache.
- Installs some commonly-used `apt` packages.
- Installs nginx.
- Creates a new site with the root pointing to `/vagrant/public`.
- Installs PostgreSQL, the `psycopg2` Python driver, and the PostGIS extension.
- Creates a new PostgreSQL database, and installs the PostGIS extension.
- Installs `pip`.
- `pip` installs the `tox`, `sphinx`, `virtualenv`, and `virtualenvwrapper` packages.

## Configuration
By default, the PostGIS database is created with the following credentials:

- Database name: `myapp`
- Database user: `myapp_dba`
- Database password: `mysecretpassword`

You can override any of the above by setting the appropriate variable:

- `postgresql_db_name`
- `postgresql_db_user`
- `postgresql_db_password`

