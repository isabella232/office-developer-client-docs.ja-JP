---
<<<<<<< ヘッド タイトル: DefinedSize プロパティ (ADO) TOCTitle: DefinedSize プロパティ (ADO) === タイトル: DefinedSize プロパティ (ADO) TOCTitle: DefinedSize プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="definedsize-property-ado"></a>DefinedSize プロパティ (ADO)
=======
# <a name="definedsize-property-ado"></a>DefinedSize プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Field](field-object-ado.md) オブジェクトのデータ容量を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

バイト数でフィールドの定義サイズを反映する長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**DefinedSize** プロパティは、 **Field** オブジェクトのデータ容量を調べるために使います。

**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。

