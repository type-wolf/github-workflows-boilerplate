## Heroku Auto Deploy Boilerplate

---

### Environment variables that need to be set in Github

1.  #### [`HEROKU_API_KEY`](https://dashboard.heroku.com/account) => APIKey for my Heroku account
2.  #### `HEROKU_APP_NAME` => Name of the Heroku application to deploy to
3.  #### `HEROKU_EMAIL` => Email address of your Heroku account

---

### How to pass environment variables to Heroku applications

1.  #### Edit [herokuDeploy.yml](.github/workflows/herokuDeploy.yml)

#### :warning: When describing environment variables in files, be sure to prefix them with `HD_`.

```yml
env:
    HD_`ENV_NAME`: ${{secrets.ENV_NAME}}
```

2.  #### Register the variables defined in ① in the Github environment variables

#### :white_check_mark: `HD` is not necessary when setting Github environment variables

---
