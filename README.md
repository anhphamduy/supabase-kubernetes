
## How to use ?

You can find the documentation inside the [chart directory](./charts/supabase/README.md)

# Steps to get real time working
- Add `ALTER USER supabase_admin WITH PASSWORD :'pgpass';` to `initdb.config.yaml`
- Dial into the pod with supabase_admin user `psql -U supabase_admin`. Then give admin perms to postgres user `ALTER ROLE postgres WITH SUPERUSER;`
- Go into the database explorer of the studio, swap out the desired tenant name under the _realtime schema.

# Azure secrets to be added to auth
```shell
GOTRUE_EXTERNAL_AZURE_ENABLED=true
GOTRUE_EXTERNAL_AZURE_CLIENT_ID=myappclientid
GOTRUE_EXTERNAL_AZURE_CLIENT_ID=tenantid
GOTRUE_EXTERNAL_AZURE_SECRET=clientsecretvaluessssh
GOTRUE_EXTERNAL_AZURE_REDIRECT_URI=http://localhost:3000
```
