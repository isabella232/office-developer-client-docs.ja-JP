---
title: Field.Attributes プロパティ (DAO)
TOCTitle: Attributes Property
description: Attributes プロパティ
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/14/2021
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 77cae4e2d4c3a09d75afa3c9f2228f72bccfd5d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626758"
---
# <a name="fieldattributes-property-dao"></a>Field.Attributes プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Field](field-object-dao.md)** オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 **Long** の値を使用します。

## <a name="syntax"></a>構文

*式* .Attributes

*式* **Field** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Field** オブジェクトの **Attributes** プロパティでは、**Field** オブジェクトを表すフィールドの特性を指定します。 **Attributes** プロパティは単一の長整数型として格納され、次の long 型定数の合計です。


|**定数**|**値**|**説明**|
|:----------|:----------|:----------|
|**dbAutoIncrField**|**16**|新しいレコードのフィールド値は、一意の長整数型の値に自動的に増分され、変更はできません (Microsoft Access ワークスペースでは、Microsoft Office Access データベース エンジン データベース テーブルでのみサポート)。|
|**dbDescending**|**1**|フィールドを降順 (Z ～ A、100 ～ 0、ん～あ) で並べ替えるオプションで、これは、 <strong>Index</strong> オブジェクトの <strong>Fields</strong> コレクションの <strong>Field</strong> オブジェクトのみに適用されます。この定数を省略すると、フィールドは昇順 (A ～ Z、0 ～ 100、あ～ん) で並べ替えられます。これは、 <strong>Index</strong> フィールドおよび <strong>TableDef</strong> フィールドの既定値です (Microsoft Access ワークスペースのみ)。|
|**dbFixedField**|**1**|フィールド サイズは固定です (数値フィールドの既定)。|
|**dbHyperlinkField**|**32768**|フィールドにはハイパーリンク情報が含まれます (メモ型フィールドのみ)。|
|**dbSystemField**|**8192**|レプリカのレプリケーション情報が保存される、削除できないタイプのフィールドです (Microsoft Access ワークスペースのみ)。|
|**dbUpdatableField**|**32**|フィールド値を変更できます。|
|**dbVariableField**|**2**|フィールド サイズは可変です (テキスト フィールドのみ)。

コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。追加された **Field** オブジェクトの場合、 **Attributes** プロパティを使用できるかどうかは、 **Fields** コレクションを含むオブジェクトによって異なります。

|**Field オブジェクトの所属先**|**Attributes プロパティの使用**|
|:----------|:----------|
|**Index** オブジェクト|**Index** オブジェクトが追加される **TableDef** オブジェクトが **Database** オブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。|
|**QueryDef** オブジェクト|読み取り専用|
|**Recordset** オブジェクト|読み取り専用|
|**Relation** オブジェクト|サポートされていません|
|**TableDef** オブジェクト|読み取り/書き込み|

複数の属性を設定する場合は、該当する定数をまとめて組み合わせることができます。無効な値は、エラーを発生させずに無視されます。

## <a name="example"></a>例

この例では、ノースウィンド データベースの **Field**、**Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

