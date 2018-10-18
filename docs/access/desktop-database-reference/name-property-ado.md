---
<<<<<<< ヘッド タイトル: 名前プロパティ (ADO) TOCTitle: 名前プロパティ (ADO) === タイトル: Name プロパティ (ADO) TOCTitle: Name プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="name-property-ado"></a>Name プロパティ (ADO)
=======
# <a name="name-property-ado"></a>Name プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

オブジェクトの名前を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

オブジェクトの名前を示す文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**Name** プロパティは、 **Command** オブジェクト、 **Property** オブジェクト、 **Field** オブジェクト、または **Parameter** オブジェクトの名前を設定または取得するために使用します。

値は、 **Command** オブジェクトでは読み取り/書き込み可能で、 **Property** オブジェクトでは読み取り専用になります。

**Field** オブジェクトの場合、 **Name** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **Name** は読み取り/書き込み可能になります。

**Parameters** コレクションに追加されていない [Parameter](parameters-collection-ado.md) オブジェクトでは、 **Name** プロパティは読み取り/書き込み可能です。追加された **Parameter** オブジェクトとその他のオブジェクトでは、 **Name** プロパティは読み取り専用です。名前はコレクション内で一意でなくてもかまいません。

オブジェクトの **Name** は、序数参照で取得でき、その後は、その名前で直接オブジェクトを参照できます。 などの場合は rstMain.Properties(20) です。名には、更新機能が得られます、このプロパティは更新の結果が、後で参照できる、rstMain.Properties("Updatability") としてこのプロパティを後で参照できます。

