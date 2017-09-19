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
- mix-deps-json elixir app
- yarn-parser node app
- gradle-parser node app
- carthageparser sinatra app
- clojars-json clojure app

### Online.net
- Postgres
- Pypi Mirror

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
- lib2issues ruby app
- dispatch ruby app
- github-firehose node app
- firehose node app
- slackin node app
- lib2slack ruby app
- npm-update-stream node app
- travis-rebuilder sinatra app
