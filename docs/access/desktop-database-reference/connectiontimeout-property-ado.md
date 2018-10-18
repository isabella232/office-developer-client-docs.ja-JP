---
<<<<<<< ヘッド タイトル: タイムアウト プロパティ (ADO) TOCTitle: タイムアウト プロパティ (ADO) === タイトル: タイムアウト プロパティ (ADO) TOCTitle: タイムアウト プロパティ (ADO)
>>>>>>> マスターの ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout プロパティ (ADO)
=======
# <a name="connectiontimeout-property-ado"></a>タイムアウト プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

接続操作を中止して、エラーを生成するまでの待機時間を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

接続が開くまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 15 です。

## <a name="remarks"></a>解説

ネットワーク トラフィックやサーバーの過度の使用が原因で接続を開く試みを中止する必要がある場合は、**Connection** オブジェクトで [ConnectionTimeout](connection-object-ado.md) プロパティを使用します。接続が開かれる前に **ConnectionTimeout** プロパティで設定した時間が経過した場合は、エラーが発生して接続の試みが取り消されます。このプロパティを 0 に設定した場合は、ADO は接続が開かれるまで無限に待機します。コードを書き込むプロバイダーが、 **ConnectionTimeout** 機能をサポートしていることを確認してください。

**ConnectionTimeout** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

