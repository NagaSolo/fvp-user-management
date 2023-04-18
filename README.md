#### Fastapi, Vue, Postgresql, flask-sqlalchemy MVP for User Management use case


##### Requirements
- Administrators can create, view, update, and delete user accounts.
- Regular users can only view and update their own accounts. 
- Administrators will get notifications of the actions done by regular users. 
- Information can be stored in a PostgreSQL database using SQLAlchemy.
- Forms must implement validation, where it should display an error message if any of the fields are invalid. 
- User can login (authentication) and be authorized.

Technologies:
- Vue 2 (Vue.js) for the front-end
- FastAPI (Python) for the back-end API
- PostgreSQL for the database
- Flask-SQLAlchemy for database ORM


##### Project Structure
- `backend`
    - `src`
        - `auth` : jwt token management
        - `database.py` : connection to database
        - `main.py` : fastapi main application
        - `models.py` : db orm model
        - `schemas.py` : API data structure schema
    - `Dockerfile` : container template for backend service
    - `requirements.txt` : packages required to run python project
- `frontend`
    - `public`: artifacts
    - `src`: source file for Vue frontend
    - `package.json` : npm packages for this project
    - `package-lock.json` : locked version of npm packages
    - `vue.config.js` : optional vue config file
    - `Dockerfile` : container template for frontend service
- `docker-compose.yaml` : containers stack to run the project
- `README.md` : documentation


##### Workflow
- Backend
    - define user schemas for API validation
    - define models for database modelling
    - configuring database migration with alembic and flask-sqlalchemy
- Frontend
    - scaffold vue frontend templates
- Containerisation
    - define services for frontend, backend, and db (port, images, volume, command)
    - define bridge network
    - define dockerfile for frontend at frontend directory
    - define dockerfile for backend at backend directory