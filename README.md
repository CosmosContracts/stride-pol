# JUNO/stJUNO PoL Multisig

This is a repository to keep track of all the multisig transactions needed to provide liquidity on the JUNO/stJUNO Osmosis' AMM pool.

# Multisig Setup

## Juno

On Juno we can use DAODAO to generate a multisig.

URL of the multisig: <https://daodao.zone/dao/juno15y8mzyzyksw2wzfcv5d67j5pzxzwj0n00agt5kk08mqwykqamheqgvsd9l>

## Stride

```bash
strided keys add rarma --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A97YGoO8s/BHRqApeBjVj1C7tiXqB2dm1q7kaUmNnJfu"}'
strided keys add brandon --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A01WIWpsLV4LUtTXbVjMUuRWY63mvudt9A51afeKA7p6"}'
strided keys add john --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"Amt1Ce/5oVEIO4avB79vuZiRZM5RW9CLAAx71hjM2d2K"}'
strided keys add reece --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApW93WeOI06jkRkctzeAiMVRRShdb+Idxmxa+3rXAlek"}'
strided keys add dimi --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApcEus7fRKwSRNNs4nlOy62fFH9Ep7lg9DQRsnx9Ht0H"}'

# Create multisig
strided keys add junopol --multisig dimi,rarma,reece,john,brandon --multisig-threshold 3

- address: stride12699lad3tfukw2ag5v4c8kx9v4cltkxkhujlw5
  name: junopol
  pubkey: '{"@type":"/cosmos.crypto.multisig.LegacyAminoPubKey","threshold":3,"public_keys":[{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"Amt1Ce/5oVEIO4avB79vuZiRZM5RW9CLAAx71hjM2d2K"},{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A01WIWpsLV4LUtTXbVjMUuRWY63mvudt9A51afeKA7p6"},{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApW93WeOI06jkRkctzeAiMVRRShdb+Idxmxa+3rXAlek"},{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApcEus7fRKwSRNNs4nlOy62fFH9Ep7lg9DQRsnx9Ht0H"},{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A97YGoO8s/BHRqApeBjVj1C7tiXqB2dm1q7kaUmNnJfu"}]}'
  type: multi
```

Address: `stride12699lad3tfukw2ag5v4c8kx9v4cltkxkhujlw5`
