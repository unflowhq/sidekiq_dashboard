# Sidekiq Dashboard

This is the repository that deploys our Sidekiq dashboard. The credentials for the server are in 1Password under "Unflow Server Sidekiq Web UI" (in the Shared vault).

https://unflow-server-sidekiq.herokuapp.com/

### Setup
1. Create the Heroku App.
2. Attach the Redis datastore from the target app. This will set the `REDIS_URL` in the app's environment variables (and keep it up to date).

```sh
heroku addons:attach unflow-server::REDIS --app unflow-server-sidekiq
```
3. Set the `USERNAME` and `PASSWORD` environment variables. These are the HTTP basic auth credentials to enter the server. It will not start without them.
4. Create/update the 1Password entry for the Sidekiq server.