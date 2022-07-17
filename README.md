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

Install CRD:
```bash
make install
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
