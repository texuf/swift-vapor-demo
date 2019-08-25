# swift-vapor-demo
just putting some swift on the heroku

Hello World here: https://docs.vapor.codes/3.0/getting-started/hello-world/

Though, I recommend using a toned down template: see https://github.com/twostraws/vapor-clean

Heroku Setup instructions here: https://elements.heroku.com/buildpacks/vapor-community/heroku-buildpack

The `vapor heroku init` is broken and fails with GeneralError(message: "Unable to locate vapor dependency"), see: https://github.com/vapor/vapor/issues/1958

I think these steps will make it work:

`echo 'web: Run serve --env production --hostname 0.0.0.0 --port $PORT' > Procfile`
`echo '5.0.1' > .swift-version`
`heroku create --buildpack vapor/vapor`
`git push heroku master`

Nice feature overview: https://www.hackingwithswift.com/articles/73/server-side-swift-kitura-vs-vapor

deploy time: 9m10.145s

check it out: https://lit-island-95059.herokuapp.com/
