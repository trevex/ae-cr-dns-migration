# AppEngine to Cloud Run DNS migration


## Deploy the applicatioe on AE
```
gcloud config set project nvoss-ae-dns-migration
gcloud app create --region=europe-west
gcloud app deploy
```

## Add a custom domain

```
curl https://nvoss-ae-dns-migration.ew.r.appspot.com/
```

Works, but we want to add our own domain, for this we follow: https://cloud.google.com/appengine/docs/standard/mapping-custom-domains

(Which boils down to `App Engine -> Settings -> Custom Domains -> Add a Custom Domain` and follow the wizard.)

## Now let's update our app and deploy to CR


