---
<<<<<<< ヘッド タイトル: OriginalValue プロパティ (ADO) TOCTitle: OriginalValue プロパティ (ADO) === タイトル: OriginalValue プロパティ (ADO) TOCTitle: OriginalValue プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="originalvalue-property-ado"></a>OriginalValue プロパティ (ADO)
=======
# <a name="originalvalue-property-ado"></a>OriginalValue プロパティ (ADO)
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

変更前のフィールドの値を表すバリアント型 ( **Variant** ) の値を返します。

## <a name="remarks"></a>解説

現在のレコードからフィールドの元の値を返すには、 **OriginalValue** プロパティを使用します。

*イミディ エイト更新モード*(でプロバイダーに変更を書き込みます、基になるデータ ソース[の更新](update-method-ado.md)メソッドを呼び出した後)、 **OriginalValue**プロパティは、変更する前に存在していたフィールドの値を返します (以後、最後の**Update**メソッドの呼び出し)。 これは、 [Value](value-property-ado.md)プロパティを置換するのには、 [CancelUpdate](cancelupdate-method-ado.md)メソッドを使用するのと同じ値です。

*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **OriginalValue**プロパティは、いずれかの前に存在していたフィールドの値を返します(つまり、最後の**UpdateBatch**メソッドを呼び出す) ために変更します。 これは、 **Value**プロパティを置換するのには、 [CancelBatch](cancelbatch-method-ado.md)メソッドを使用するのと同じ値です。 [UnderlyingValue](underlyingvalue-property-ado.md)プロパティを使用してこのプロパティを使用する場合は、バッチ更新で発生した競合を解決できます。

## <a name="record"></a>Record

[Record](record-object-ado.md) オブジェクトの場合、 **Update** を呼び出す前に追加されたフィールドの [OriginalValue](update-method-ado.md) プロパティは空になります。

