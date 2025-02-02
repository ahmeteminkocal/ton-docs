# API Types

**High availability blockchain APIs are the core element of secure, convenient and fast development of useful applications on TON.**

- [TON HTTP API](/develop/dapps/apis/toncenter) — API that allows to work with the _indexed blockchain information_.
- [TON ADNL API](/develop/dapps/apis/adnl) — secure API to communicate with TON, based on ADNL protocol.

## Third party APIs
- [tonapi.io](https://docs.tonconsole.com/tonapi/api-v2) - fast indexed API which provides basic data about accounts, transactions, blocks, application-specific data about NFT, Auctions, Jettons, TON DNS, Subscriptions. It also provides annotated data on transaction chains.
- [dton.io](https://dton.io/graphql/) - GraphQL API with that can provide data about accounts, transactions and blocks, as well as application-specific data about NFT, Auctions, Jettons and TON DNS.
- [ton-api-v4](https://mainnet-v4.tonhubapi.com) - another lite-api focused on speed via aggressive cashing in CDN.
- [evercloud.dev](https://ton-mainnet.evercloud.dev/graphql) - GraphQL API for basic queries in TON.
- [everspace.center](https://everspace.center/toncoin) - Simple RPC API for accessing TON Blockchain.


## Additional APIs

### Toncoin rate APIs

* https://tonapi.io/v2/rates?tokens=ton&currencies=ton%2Cusd%2Crub
* https://coinmarketcap.com/api/documentation/v1/ 
* https://apiguide.coingecko.com/getting-started


### Address Convert APIs


:::info
It is preferable to convert address via local algorithm, read more in the [Addresses](/learn/overviews/addresses) section of documentation.
:::


#### From Friendly to Raw form

/api/v2/unpackAddress

Curl
```curl
curl -X 'GET' \
'https://toncenter.com/api/v2/unpackAddress?address=EQApAj3rEnJJSxEjEHVKrH3QZgto_MQMOmk8l72azaXlY1zB' \
-H 'accept: application/json'
```

Response body
```curl
{
"ok": true,
"result": "0:29023deb1272494b112310754aac7dd0660b68fcc40c3a693c97bd9acda5e563"
}
```

#### From Friendly to Raw form

/api/v2/packAddress

Curl
```curl
curl -X 'GET' \
'https://toncenter.com/api/v2/packAddress?address=0%3A29023deb1272494b112310754aac7dd0660b68fcc40c3a693c97bd9acda5e563' \
-H 'accept: application/json'
```

Response body
```json
{
  "ok": true,
  "result": "EQApAj3rEnJJSxEjEHVKrH3QZgto/MQMOmk8l72azaXlY1zB"
}
```



## See Also
* [TON HTTP API](/develop/dapps/apis/toncenter)
* [List of SDKs](/develop/dapps/apis/sdk)
* [TON Cookbook](/develop/dapps/cookbook)
