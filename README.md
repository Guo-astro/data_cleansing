### Setup auth


- Go to gcp console, open a cloud shell
```bash
gcloud iam service-accounts create bqplayground --display-name "bqplayground"
gcloud projects add-iam-policy-binding $DEVSHELL_PROJECT_ID --member serviceAccount:bqplayground@$DEVSHELL_PROJECT_ID.iam.gserviceaccount.com --role roles/bigquery.admin
gcloud iam service-accounts keys create bqplayground-admin.json --iam-account=bqplayground@$DEVSHELL_PROJECT_ID.iam.gserviceaccount.com
```