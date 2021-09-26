---
title: Field.ForeignName プロパティ (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cbf586d3c07ccfd01a170efd4efaaacc45385c36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626687"
---
# <a name="fieldforeignname-property-dao"></a>Field.ForeignName プロパティ (DAO)


**適用先**: Access 2013、Office 2013

リレーションシップの主テーブルのフィールドに対応する、外部キー側のテーブルの **[Field](field-object-dao.md)** オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .ForeignName

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**[Database](relation-object-dao.md)** オブジェクトに **[Relation](database-object-dao.md)** オブジェクトが追加されておらず、 **Relation** オブジェクトに **Field** オブジェクトが追加されている場合、 **ForeignName** プロパティは値の取得および設定が可能です。データベースに **Relation** オブジェクトを追加すると、 **ForeignName** プロパティは値の取得のみ可能になります。

**Relation** オブジェクトの **Fields** コレクションに属する **Field** オブジェクトのみが、 **ForeignName** プロパティをサポートできます。

**Field** **[オブジェクトの](connection-name-property-dao.md)** Name プロパティと **ForeignName** プロパティ設定では、リレーションシップのプライマリ テーブルと外部テーブルの対応するフィールドの名前を指定します。 **[Relation オブジェクトの](relation-table-property-dao.md)** Table プロパティ **[と ForeignTable](relation-foreigntable-property-dao.md)** プロパティの設定によって、リレーションシップのプライマリ テーブルと外部テーブルが決定されます。 

たとえば、ValidParts テーブルに有効な部品コード (PartNo という名前のフィールド) の一覧が格納されている場合、OrderItem テーブルに部品コードが入力されるときには、その部品コードが ValidParts テーブルに既に存在している必要があるという、OrderItem テーブルとのリレーションシップを設定できます。 パーツ コードが ValidParts テーブルに存在しない場合 **、Relation** オブジェクトの **[Attributes](field-attributes-property-dao.md)** プロパティを **dbRelationDontEnforce** に設定していない場合は、トラップ可能なエラーが発生します。

この例では、ValidParts テーブルが外部キー側のテーブルになるため、 **Relation** オブジェクトの **ForeignTable** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **Table** プロパティが OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。

## <a name="example"></a>例

次の例では、 **Table**、 **ForeignTable**、および **ForeignName** の各プロパティによる 2 つのテーブル間の **Relation** の条件を定義する方法を示します。

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
