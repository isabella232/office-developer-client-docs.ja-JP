---
title: Field.ForeignName プロパティ (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 542e4f3f2b0f2b3a88c5f4d358e36a4faa196a7b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869723"
---
# <a name="fieldforeignname-property-dao"></a>Field.ForeignName プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

リレーションシップの主テーブルのフィールドに対応する、外部キー側のテーブルの **[Field](field-object-dao.md)** オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。ForeignName

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**[Database](relation-object-dao.md)** オブジェクトに **[Relation](database-object-dao.md)** オブジェクトが追加されておらず、 **Relation** オブジェクトに **Field** オブジェクトが追加されている場合、 **ForeignName** プロパティは値の取得および設定が可能です。データベースに **Relation** オブジェクトを追加すると、 **ForeignName** プロパティは値の取得のみ可能になります。

**Relation** オブジェクトの **Fields** コレクションに属する **Field** オブジェクトのみが、 **ForeignName** プロパティをサポートできます。

[Field](connection-name-property-dao.md) オブジェクトの ****Name**** プロパティおよび **ForeignName** プロパティの設定値によって、リレーションシップの主テーブルと外部キー側のテーブル内にある対応するフィールドの名前が指定されます。 [Relation](relation-table-property-dao.md) オブジェクトの [**Table**](relation-foreigntable-property-dao.md) プロパティおよび ****ForeignTable**** プロパティの設定値によって、リレーションシップの主テーブルと外部キー側のテーブルが決まります。

たとえば、ValidParts テーブルに格納された有効な部品コード (フィールド名 PartNo 内) のリストがあり、OrderItem テーブルに部品コードが入力された場合に OrderItem テーブルとのリレーションシップを確立するには、ValidParts テーブルにその部品コードが既に存在している必要があります。ValidParts テーブルに部品コードがなく、 [Relation](field-attributes-property-dao.md) オブジェクトの ****Attributes**** プロパティが **dbRelationDontEnforce** に設定されていない場合、トラップ可能なエラーが発生します。

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
