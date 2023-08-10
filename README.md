# Optimize camera locations
An approach using differential evolution to optimize surveillance camera locations in urban settings

Requirements:

- PostgreSQL 14.5 + PostGIS 3.2.3
- Python 3.11.4+

1. Install Postgres + PostGIS
2. Connect to DB: `psql -h localhost -p 5432 -d postgres -U postgres` (type postgres user password)
3. Create database "evolucion_diferencial": `CREATE DATABASE optimize_camera_locations;`
4. Select database : `\c optimize_camera_locations`
5. Enable PostGIS: `CREATE EXTENSION postgis;`
6. Exit psql: `\q`
4. Restore database: `psql -U postgres -d optimize_camera_locations -f optimize_camera_locations.sql`

Install Python (conda), add `conda-forge` channel, create new environment, if desired, and install dependencies:

1. `conda config --add channels conda-forge`
2. `conda config --set channel_priority strict`
3. `conda install --name `_myenv_` --file environment.yaml`
4. If necessary, install `t4gpd` manually with: `pip install t4gpd-0.3.0.tar.gz`

Launch Jupyter Lab (`jupyter lab`) or Jupyter Notebook (`jupyter notebook`) and execute notebook's cells.