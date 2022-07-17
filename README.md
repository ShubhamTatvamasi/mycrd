# mycrd

Initalize kubebuilder:
```bash
kubebuilder init \
  --domain shubhamtatvamasi.com \
  --repo github.com/ShubhamTatvamasi/mycrd
```

Create new API:
```bash
kubebuilder create api \
  --version v1 \
  --group demo \
  --kind DemoVolume
```
---

Generate CRD:
```bash
make generate
```

Generate webhooks:
```bash
make manifests
```

Install Custom Resource Definition:
```bash
make install
```

Install Custom Resource:
```bash
kubectl apply -f config/samples/
```

Delete Custom Resource:
```bash
kubectl delete -f config/samples/
```

Run your controller:
```bash
make run
```

---

### Kustomize for M1

Initalize with plugins:
```bash
kubebuilder init \
  --domain shubhamtatvamasi.com \
  --repo github.com/ShubhamTatvamasi/mycrd \
  --plugins=kustomize/v2-alpha,base.go.kubebuilder.io/v3
```

Change kustomize version in `Makefile`:
```Makefile
KUSTOMIZE_VERSION ?= v4.5.5
```
