# fotohaus-triage

## listing an item

```mermaid
graph TD
    A([item ready for listing]) --> B[enter listing in HQ]
    B --> C{listing approved}
    C -- yes --> D[create listing]
    C -- no --> E[cancel]
    E -- make some changes --> B
    D --> F[/Shopware listing/]
    D --> G[/Ebay listing/]
    D --> H[/Ricardo listing/]
```
