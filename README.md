# svelte + django

This is an example app that uses Svelte for it's frontend and Django on the backend.

The Svelte frontend uses Webpack (instead of Rollup) for bundling. It uses [this](https://github.com/sveltejs/template-webpack) template.

We proxy our `/api` requests through to the Django backend using Webpack's devserver, as shown [here](https://webpack.js.org/configuration/dev-server/#devserverproxy).

It also uses [Faker](https://github.com/joke2k/faker) to generate fake name's and addresses for demonstration.

## How to use

Install the dependencies for the frontend...

```bash
cd frontend
npm install
```

...and the dependencies for the backend in a python virtual environment...

```bash
cd backend
python3 -m venv env
. env/bin/activate
pip3 install -r requirements.txt
```

...then start the frontend devserver...

```bash
npm run dev
```

...open another terminal to start the django server:

```bash
python manage.py runserver
```
