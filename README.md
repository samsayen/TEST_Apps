# TEST_Apps

Use the CF cli
https://docs.cloudfoundry.org/cf-cli/install-go-cli.html


    cf login
    cf marketplace
    cf spaces
    cf domains
    cf org <org name>
    cf org-users <org>
    cf apps
    cf services
    cf create-service <service> <plan> <name you set>
    cf delete-service <service name>
    cf service <service name>  , bunch of info, bindings, dashboard, etc

CF app example
https://github.com/epoelke/multibuildpack-test-app

    cf push <app-name>
    cf restart <app-name>
    cf restage <app-name>
    cf delete <app name>

Bind an app to a service

    cf bind-service <app name> mydb
    cf restart <app name>

Delete a service

    cf services
    cf delete-service <service-name>

Deploy APP with build pack
    Go within the app's directory
    cf push flaskapp -b https://github.com/cloudfoundry/python-buildpack.git -u none -c "app.py"
