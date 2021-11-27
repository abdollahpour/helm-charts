Standard chart for micro-image-manager.

# Install

Here is an example:

    helm repo add abdollahpour https://abdollahpour.github.io/helm-charts
        helm install \
            --set "ingress.hosts[0].host=your-domain.com" \
            --set "ingress.hosts[0].publicManagement=true" \
            --set "persistence.enabled=false" \
            my-micro-image-manager abdollahpour/micro-image-manager

NEVER use `ingress.publicManagement=true` on production. It's just for tests.
Use any storage class that is available on your cluster for image storage.
For more information check [micro-image-manager documentation](https://github.com/abdollahpour/micro-image-manager).

For list of full values and comments please check [values.yaml](values.yaml).
