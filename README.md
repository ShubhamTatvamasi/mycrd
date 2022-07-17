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
