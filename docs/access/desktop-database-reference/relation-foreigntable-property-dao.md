---
title: Relation.ForeignTable プロパティ (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ad95e1ff7402ce9115421554c5a08b31a6145ac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878662"
---
# <a name="relationforeigntable-property-dao"></a>Relation.ForeignTable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

リレーションシップの外部テーブルの名前を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。外部テーブル

*式***Relation**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

このプロパティは、新しい **[Relation](relation-object-dao.md)** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Relations**](relations-collection-dao.md) コレクション内の既存の **Relation** オブジェクトの場合は値の取得のみ可能です。

**Relation** オブジェクトの **ForeignTable** プロパティの設定値は、外部テーブルまたはクエリを表す **[TableDef](connection-name-property-dao.md)** オブジェクトまたは **[QueryDef](tabledef-object-dao.md)** オブジェクトの **[Name](querydef-object-dao.md)** プロパティの設定値で、 **[Table](relation-table-property-dao.md)** プロパティの設定値は、主テーブルまたはクエリを表す **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値です。

たとえば、ValidParts テーブルに格納された有効な部品コード (フィールド名 PartNo 内) のリストがあり、OrderItem テーブルに部品コードが入力された場合に OrderItem テーブルとのリレーションシップを確立するには、ValidParts テーブルにその部品コードが既に存在している必要があります。ValidParts テーブルに部品コードがなく、 [Relation](field-attributes-property-dao.md) オブジェクトの ****Attributes**** プロパティが **dbRelationDontEnforce** に設定されていない場合、トラップ可能なエラーが発生します。

この例では、ValidParts テーブルが主テーブルになるため、 **Relation** オブジェクトの **Table** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **ForeignTable** プロパティが OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。

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
