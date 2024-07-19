eks terraform
-------------

for ur user for demo example i used:
- create terraformers group in iam with adminaccess role (you can prolly adjust roles better but for example sake)
- put your user into it
- `aws configure` as your user

tofu init
tofu plan
tofu apply

```
aws eks --region $(tofu output -raw region) update-kubeconfig \
    --name $(tofu output -raw cluster_name)
```
