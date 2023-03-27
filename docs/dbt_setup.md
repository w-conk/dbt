## DBT Installation on Ubuntu Server

Notes:
- Need SSH access for your DO instance (done)
- sudo access is required

1. SSH into server
2. Create virtual python environment named `dbtenv` in the right directory (make one i guess)
```
sudo -u will virtualenv -p python3.9 /path/to/wherever/dbtenv
```
3. Navigate to newly-created pyenv
```
cd /path/to/wherever/dbtenv
```
4.Activate environment
```
source bin/activate
```
5. Install or update to latest version of setuptools
```
sudo pip install --upgrae pip wheel setuptools
```
6. Install DBT core with PostgreSQL adapter
```
sudo pip install dbt-postgres
```
7. Check to make sure the latest version of dbt is installed
```
dbt --version
```
8. Create dbt project with `my_dbt_project` as name
```
sudo dbt init my_dbt_project
```
9. Navigate to new project
```
cd my_dbt_project
```
10. Edit `dbt_project` YAML file and set relevant values as required
```
sudo nano dbt_project.yml
```
11. Create `profiles` YAML file in a `.dbt` directory
```
sudo cat > ~/.dbt/profiles.yml
```
12. Edit newly created file and set relevant configuration
