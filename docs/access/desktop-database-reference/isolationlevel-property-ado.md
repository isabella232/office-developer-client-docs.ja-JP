---
<<<<<<< ヘッド タイトル: IsolationLevel プロパティ (ADO) TOCTitle: IsolationLevel プロパティ (ADO) === タイトル: IsolationLevel プロパティ (ADO) TOCTitle: IsolationLevel プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="isolationlevel-property-ado"></a>IsolationLevel プロパティ (ADO)
=======
# <a name="isolationlevel-property-ado"></a>IsolationLevel プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Connection](connection-object-ado.md) オブジェクトの分離レベルを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[IsolationLevelEnum](isolationlevelenum.md) の値を設定または取得します。既定値は **adXactChaos** です。

## <a name="remarks"></a>解説

**IsolationLevel** プロパティでは、 **Connection** オブジェクトの分離レベルを設定します。設定値は、次に [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを呼び出すまで有効になりません。要求した分離レベルを使用できない場合、プロバイダーはその次に高い分離レベルを返します。

**IsolationLevel** プロパティは読み取り/書き込み可能です。

**リモート データ サービスの使用法**クライアント側の Connection オブジェクトで使用すると、 **IsolationLevel**プロパティは**adXactUnspecified**にのみ設定できます。

ユーザーは、クライアント側のキャッシュ上の接続されていない **Recordset** オブジェクトで作業するため、マルチユーザーの場合は問題になることがあります。たとえば、2 人のユーザーが同じレコードを更新しようとした際、リモート データ サービスは単純に先に操作を行ったユーザーの更新を受け付けます。2 番目のユーザーの更新要求はエラーになって失敗します。

