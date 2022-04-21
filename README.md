


## API: 取得擁有此NFT的會員
[範例](https://node1.apgame001.com/nft/0x2953399124f0cbb46d2cbacd8a89cf0599974963/61007109323655003125047866664436596704083617370037353424924359052686341963777/owners)

- 格式
```bash
https://node1.apgame001.com/nft/{contractAddress}/{tokenId}/owners
```

- 輸入
  - contractAddress: 智能合約地址
  - tokenId: NFT的TokenId

- 輸出
```bash
{
  total: 1, // 總數量
  result: [
    {
      ownerAddress: '0x2c1183487c6ca1e1a159257b481d25114169916f', // 會員地址
      amount: 1 // 擁有數量
    }
  ],
  contractAddress: '0x2953399124f0cbb46d2cbacd8a89cf0599974963', // 智能合約地址
  tokenId: '61007109323655003125047866664436596704083617370037353424924359052686341963777', // NFT的TokenId
  status: 'ok' // 表示成功
}
```

## API: 取得會員擁有的NFT
[範例](https://node1.apgame001.com/0x2c1183487c6ca1e1a159257b481d25114169916f/nft/0x2953399124f0cbb46d2cbacd8a89cf0599974963)

- 格式
```bash
https://node1.apgame001.com/{ownerAddress}/nft/{contractAddress}
```

- 輸入
  - ownerAddress: 會員地址
  - contractAddress: 智能合約地址

- 輸出
```bash
{
  total: 1, // 總數量
  result: [
    {
      tokenId: '61007109323655003125047866664436596704083617370037353424924359052686341963777', // NFT的TokenId
      amount: 1 // 擁有數量
    }
  ],
  contractAddress: '0x2953399124f0cbb46d2cbacd8a89cf0599974963', // 智能合約地址
  ownerAddress: '0x2c1183487c6ca1e1a159257b481d25114169916f', // 會員地址
  status: 'ok' // 表示成功
};
```


## API: 資料同步(每當新增NFT則必須呼叫此API)
```bash
https://node1.apgame001.com/sync
```

- 輸入
  無
  
- 輸出
  無
