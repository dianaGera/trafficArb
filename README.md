# trafficArb
> Client requested to create a single page with contact form and description section for product
> [11.04.2023] "Get loan in Georgia" deployed [>>>](https://credit-georgia.info/ge) 

# Backend Set Up
##### Create and activate virtual environment:
```bash
python3 -m venv venv
venv\Scripts\activate (Windows in cmd)
source venv/bin/activate (Linux)
```

##### Install dependensies:
```bash
pip install -r requirements.txt
```

##### Envs:
> find .env.sample file in root folder and rename to .env

##### Init DB:
```bash
flask db init
flask db migrate
flask db upgrade
```

##### Run server in development mode:
```bash
flask --app app --debug run
```

# Frontend Set Up 
##### Install dependencies:
``` bash
sudo apt-get install npm (Linux)
```
(For Windows) Download and install Node.js from the official [website](https://nodejs.org/en/download/)
``` bash
npm i tailwindcss
```
##### Build tailwind css:
``` bash
npx tailwindcss -i ./static/css/index.css -o ./static/css/output.css
```
##### Watch for tailwind css updates:
``` bash
npx tailwindcss -i ./static/css/index.css -o ./static/css/output.css --watch
```



# Examples
[Figma Design](./static/pdf/AbritrageTraffic.pdf)


# v1.0.0 Release Notes:

### New Features
* Main page with a form for getting user contact data and a description section for the product, written on **templates (Jinja2) + JavaScript + Ajax**
* Incorporated the use of **SQLAlchemy Alembic** for managing DB migration and ORM.
* Integrated **Flask-Admin** to provide an easy-to-use interface for managing user data and other backend tasks.
* Added **Flask Auth** to ensure secure user authentication and authorization.
* Implemented **translation** functionality that supports 4languages (GE, EN, UA, RU).
* Deployed on **DigitalOcean**


### v2.0.0 Planned Features
* Use **React and REACT Dynamic Forms** instead of templates
* Use **Postgres** instead of **SQLite3**
* Use **Google OAuth2/3** instead of **Flask Auth**
* Use  **Flask Sleek and Flask Sleek Dashboard**
* Containerization **Docker**
* Use **Poetry** for better dependency managment
