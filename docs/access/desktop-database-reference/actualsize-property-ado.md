---
<<<<<<< ヘッド タイトル: ActualSize プロパティ (ADO) TOCTitle: ActualSize プロパティ (ADO) ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: 48542949 ms.date: 2015/09/18 mtps_version: v =office.15
---

# <a name="actualsize-property-ado"></a>ActualSize プロパティ (ADO)
=== タイトル: ActualSize プロパティ (ADO) TOCTitle: ActualSize プロパティ (ADO) ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: 48542949 ms.date: 2018/10/16 mtps_version: v=office.15
---

# <a name="actualsize-property-ado"></a>ActualSize プロパティ (ADO)
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

フィールドの値の実際の長さを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

長整数型 ( **Long** ) の値を返します。プロバイダーによっては、このプロパティを BLOB データの予約空間に設定することができる場合もあり、この場合の既定値は 0 です。

## <a name="remarks"></a>解説

**ActualSize** プロパティを使用すると、 [Field](field-object-ado.md) オブジェクトの値の実際の長さを取得できます。どのフィールドについても、 **ActualSize** プロパティは値の取得のみ可能です。ADO が **Field** オブジェクトの値の長さを判断できない場合は、 **ActualSize** プロパティからは **adUnknown** が返されます。

<<<<<<< **ActualSize**のヘッドし、 [DefinedSize](definedsize-property-ado.md)プロパティは、次の例のように、異なります。 **adVarChar** 型で宣言された **Field** オブジェクトで最大長が 50 文字の場合、 **DefinedSize** プロパティは 50 という値を返しますが、 **ActualSize** プロパティは、カレント レコードのそのフィールドに格納されているデータの長さを返します。 255 バイトより大きい **DefinedSize** を持つ **Fields** は、可変長列として扱われます。
===、 **ActualSize**プロパティと[DefinedSize](definedsize-property-ado.md)プロパティは、異なります。 **adVarChar** 型で宣言された **Field** オブジェクトで最大長が 50 文字の場合、 **DefinedSize** プロパティは 50 という値を返しますが、 **ActualSize** プロパティは、カレント レコードのそのフィールドに格納されているデータの長さを返します。 255 バイトより大きい **DefinedSize** を持つ **Fields** は、可変長列として扱われます。
>>>>>>> master

