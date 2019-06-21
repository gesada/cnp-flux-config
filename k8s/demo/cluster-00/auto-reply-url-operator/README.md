# auto-reply-url-operator

See: https://github.com/hmcts/auto-reply-urls

This operator will add reply urls to the application configure in Azure AD based off ingress events

Configure it with:
```bash
$ kubectl create secret generic auto-reply-urls-creds --from-literal azure_client_id=****** --from-literal azure_client_secret=********* --from-literal azure_tenant_id=**** --dry-run -o yaml > /tmp/creds.yaml
kubeseal --format=yaml --cert=k8s/demo/pub-cert.pem <  /tmp/creds.yaml >  k8s/demo/cluster-00/auto-reply-url-operator/creds.yaml

```