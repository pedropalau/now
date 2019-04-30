# Missing Environment Variables While Developing

#### Why This Error Occurred
You ran `now dev` inside a project that contains a `now.json` file with `env` or `build.env` properties that use [Now Secrets](https://zeit.co/docs/v2/deployments/environment-variables-and-secrets).

In order to use environment variables in your project locally that have values defined using the Now Secrets format (e.g. `@my-secret-value`), you will need to provide the value as an environment variable using a `.env` or `.env.build` file.

We require this to ensure your app works as you intend it to, in the Now Dev environment, and to provide you with a way to mirror or seperate private environment variables within your applications, for example when connecting to a database.

Read below for how to address this error.

#### Possible Ways to Fix It

The error message will list environment variables that are required and which file they are required to be included in (either `.env` or `.env.build`).

If the file does not exist yet, please create the file that the error message mentions and insert the missing environment variable into it.

For example, if the error message shows that the environment variable `TEST` is missing from `.env`, then the `.env` file should look like this:

```
TEST=value
```

In the above example, `TEST` represents the name of the environment variable and `value` its value.

For more information on Environment Variables in development, [see the documentation](https://zeit.co/docs/v2/development/environment-variables/).