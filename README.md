# fotohaus-triage

## listing an item

### api

| platform | method | possible |
| -------- | ------ | -------- |
| shopware | v5: https://developers.shopware.com/developers-guide/rest-api/api-resource-article/#post-(create) <br> v6: https://shopware.stoplight.io/docs/admin-api/ZG9jOjEyMzA4NTQ5-writing-entities#creating-entities | ✅ |
| ebay | https://developer.ebay.com/api-docs/sell/inventory/resources/inventory_item/methods/bulkCreateOrReplaceInventoryItem <br> https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/createOffer | ✅ |
| ricardo | https://ws.ricardo.ch/RicardoApi/documentation/html/M_Ricardo_Contracts_ISellService_CreateArticle.htm <br> https://ws.ricardo.ch/RicardoApi/documentation/html/M_Ricardo_Contracts_ISellService_AddArticlePictures.htm | ✅ |

### flow

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

## deleting and item

### api

| platform | method | possible |
| -------- | ------ | -------- |
| shopware | v5: https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer <br> v6: https://shopware.stoplight.io/docs/admin-api/ZG9jOjEyMzA4NTQ5-writing-entities#deleting-entities | ✅ |
| ebay | https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/deleteOffer | ✅ |
| ricardo | https://ws.ricardo.ch/RicardoApi/documentation/html/M_Ricardo_Contracts_ISellService_CloseArticle.htm | ✅ |

## update / pause and item

### api

| platform | method | possible |
| -------- | ------ | -------- |
| shopware | v5: https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer <br> v6: https://shopware.stoplight.io/docs/admin-api/ZG9jOjEyMzA4NTQ5-writing-entities#updating-entities | ✅ |
| ebay | https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/withdrawOffer <br> https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer | ✅ |
| ricardo | https://ws.ricardo.ch/RicardoApi/documentation/html/M_Ricardo_Contracts_ISellService_ModifyArticle.htm <br> https://ws.ricardo.ch/RicardoApi/documentation/html/M_Ricardo_Contracts_ISellService_RepublishArticle.htm | ✅ |

## trigger on sale

### api

### api

| platform | method | possible |
| -------- | ------ | -------- |
| shopware |  | ✅ |
| ebay |  | ✅ |
| ricardo |  | ✅ |
