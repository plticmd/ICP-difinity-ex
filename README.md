## The way of rapid deproy Sample Canisters {
#### to Local & Playground.

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
キャニスターをローカルへデプロイします。キャニスターをローカルへデプロイする場合、ローカル レプリカが実行されている必要があります。 
```
dfx start --background
```
で開始します。
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

}

-----------------------

### サイクル

キャニスター スマート コントラクトは、サイクルを燃焼させることで、消費されたリソース (ストレージ、メッセージング、実行等) の支払いを行います。開発者は、[dfx](https://internetcomputer.org/docs/current/developer-docs/defi/cycles/converting_icp_tokens_into_cycles)を使用して ICP トークンをサイクルへ変換できます。

まず ICPトークン を取引所等で入手し、アカウントへ転送します。ICP トークンを転送するアカウントの確認は以下のコマンド実行。

```
dfx ledger account-id
```
ICP元帳上のアカウント番号が表示されます。

5～10 米ドル相当のトークンがあれば十分です。

ICP 元帳アカウントへ ICP トークンをいくつか取得したら、次のコマンドを使用して残高を確認できます。
```
dfx ledger --network ic balance
```

(結果 : 0.00000000 ICP)

ICP トークンを取得したら以下のコマンドでサイクルへ変換します。
```
dfx cycles convert --amount AMOUNT --network ic
```
このワークフローは、Cycles 元帳機能を利用します。将来、Cycles ウォレットは dfx から削除されます。

以下のコマンドでサイクルのバランスを確認します。
```
dfx cycles balance --network ic
```
以下のような内容が出力されます。
6.951 TC (trillion cycles
