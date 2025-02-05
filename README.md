## The way of rapid deproy Sample canisters 
#### to Local & Playground

See [motoko/life](https://github.com/plticmd/ICP-difinity-ex/tree/master/motoko/life), [motoko/counter](https://github.com/plticmd/ICP-difinity-ex/tree/master/motoko/counter), [motoko/icrc2-swap](https://github.com/plticmd/ICP-difinity-ex/tree/master/motoko/icrc2-swap), [hosting/photo-storage](https://github.com/plticmd/ICP-difinity-ex/tree/master/hosting/photo-storage), [archive/motoko/hello](https://github.com/plticmd/ICP-difinity-ex/tree/master/archive/motoko/hello),

[NotionPage](https://petal-tarsal-2b3.notion.site/Sample-Canister-Deploy-190e519d441a80b1a942d2b1b8283023)

<img width="1280" alt="スクリーンショット 2025-02-04 22 14 00" src="https://github.com/user-attachments/assets/b364e006-c0ca-49f5-9e12-a38f75ff79c6" />

<img width="1280" alt="スクリーンショット 2025-02-05 4 56 23" src="https://github.com/user-attachments/assets/71baefa8-0391-4684-a6aa-697a683ca910" />

<img width="1280" alt="スクリーンショット 2025-02-05 8 52 15" src="https://github.com/user-attachments/assets/05f532ca-b15f-4bb9-9183-17a1d8904d94" />

注意）
.dfxファイルは gitignore なのでデプロイ作業をしてWASM生成してください。


### 🌼 deploy方法4種
```
$ dfx deploy <canister-name>: 
```
キャニスターをローカルへデプロイします。キャニスターをローカルへデプロイする場合、ローカル レプリカが実行されている必要があります。 dfx start --backgroundで開始します。
```
$ dfx deploy <canister-name> --network=playground: 
```
キャニスターをplaygroundへデプロイします。pllayroundへキャニスターを設置するのは無料ですが、キャニスターは一時的なものであり20 分後に削除されます。
```
$ dfx deploy <canister-name> --network=ic: 
```
キャニスターをメインネットへデプロイします。メインネットへキャニスターをデプロイするには、[サイクルの](https://internetcomputer.org/docs/current/developer-docs/gas-cost)コストがかかります。
```
$ dfx deploy --network=ic: 
```
プロジェクトdfx.jsonファイル内のすべてのキャニスターをメインネットへデプロイします。
