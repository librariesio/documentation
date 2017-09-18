# Infrastructure

![Overview of Libraries.io architecture](infrastructure.png "Libraries.io Architecture")

Where all the services and APIs currently exist:

### Heroku
- Sendgrid email bronze addon

### Scaleway
- Rails application
- Elasticsearch
- Redis
- memcached
- Sidekiq workers
- cron
- pydeps
- cocoapods-api

### Online.net
- Postgres

### Bugsnag
- error reporting

### Appsignal
- Performance monitoring

### Cloudflare
- DNS
- SSL

### DNSimple
- Registrar

### Google Apps
- @libraries.io email

### Amazon S3
- backups
- sitemap hosting

### Other Heroku apps
- firehose node app
- github sinatra app
- carthageparser sinatra app
- clojars-json clojure app
- firstprbot twitter bot
- dispatch ruby app
- github-firehose node app
- libby the libraries hubot
- justopensourced twitter bot
- mix-deps-json elixir app
- travis-rebuilder sinatra app
- npm-update-stream node app
- yarn-parser node app
- gradle-parser node app
