---
<<<<<<< ヘッド タイトル: NumericScale プロパティ (ADO) TOCTitle: NumericScale プロパティ (ADO) === タイトル: NumericScale プロパティ (ADO) TOCTitle: NumericScale プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="numericscale-property-ado"></a>NumericScale プロパティ (ADO)
=======
# <a name="numericscale-property-ado"></a>NumericScale プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Parameter](parameter-object-ado.md) オブジェクトまたは [Field](field-object-ado.md) オブジェクトの数値の桁数を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

数値の小数点以下の桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**NumericScale** プロパティは、数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値の小数点以下の桁数を取得するために使用します。

**Parameter** オブジェクトでは、 **NumericScale** は読み取り/書き込み可能です。

**Field** オブジェクトの場合、 **NumericScale** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **NumericScale** は読み取り/書き込み可能になります。

