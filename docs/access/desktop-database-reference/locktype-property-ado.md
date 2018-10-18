---
<<<<<<< ヘッド タイトル: LockType プロパティ (ADO) TOCTitle: LockType プロパティ (ADO) === タイトル: LockType プロパティ (ADO) TOCTitle: LockType プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: 48543589 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="locktype-property-ado"></a>LockType プロパティ (ADO)
=======
# <a name="locktype-property-ado"></a>LockType プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

編集時にレコードに適用されるロックの種類を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[LockTypeEnum](locktypeenum.md) の値を設定または取得します。既定値は **adLockReadOnly** です。

## <a name="remarks"></a>解説

プロバイダーが **Recordset** を開くときに使用するロックの種類は、 [LockType](recordset-object-ado.md) プロパティを使用して事前に設定します。開いている **Recordset** オブジェクトで使用されているロックの種類は、このプロパティを取得することで確認できます。

プロバイダーによってはすべての種類のロックをサポートしていないものもあります。要求した **LockType** 設定をプロバイダーがサポートしていない場合は、他の種類のロックに置き換えられます。 **Recordset** オブジェクトで実際に使用可能なロック機能を調べるには、 [adUpdate](supports-method-ado.md) と **adUpdateBatch** で **Supports** メソッドを使用します。

**CursorLocation** が [adUseClient](cursorlocation-property-ado.md) に設定されている場合、 **adLockPessimistic** 設定はサポートされません。サポートされていない値を設定してもエラーにはなりませんが、サポートされる **LockType** のうち、最も近いロックが使用されます。

**LockType** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

**リモート データ サービスの使用法**クライアント側の Recordset オブジェクトで使用すると、 **LockType**プロパティは**adLockBatchOptimistic**にのみ設定できます。

