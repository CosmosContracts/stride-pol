# How to sign

## Compile strided

```bash
git clone https://github.com/Stride-Labs/stride.git
cd stride
make install
```

## Add multisig information
```
strided keys add rarma --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A97YGoO8s/BHRqApeBjVj1C7tiXqB2dm1q7kaUmNnJfu"}'
strided keys add brandon --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"A01WIWpsLV4LUtTXbVjMUuRWY63mvudt9A51afeKA7p6"}'
strided keys add john --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"Amt1Ce/5oVEIO4avB79vuZiRZM5RW9CLAAx71hjM2d2K"}'
strided keys add reece --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApW93WeOI06jkRkctzeAiMVRRShdb+Idxmxa+3rXAlek"}'
strided keys add dimi --pubkey '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"ApcEus7fRKwSRNNs4nlOy62fFH9Ep7lg9DQRsnx9Ht0H"}'

strided keys add junopol --multisig dimi,rarma,reece,john,brandon --multisig-threshold 3

```

**Note:** Don't specify the pubkey flag for your own key. Use the --recover or --ledger flag to import it.

## Signing

```bash
cd stride/0
strided tx sign tx_raw.json --from dimi --multisig junopol --output-document dimi_signed.json
```

## Collecting signatures

Once you have all the signatures required (3/5) put the different jsons in the same folder

```bash
strided tx multisign tx_raw.json junopol dimi_signed.json rarma_signed.json brandon_signed.json
```
