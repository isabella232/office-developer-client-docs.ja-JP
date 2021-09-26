---
title: Relation.Table プロパティ (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 90faf649c625cee7c3ea104119218a469a6be6ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611638"
---
# <a name="relationtable-property-dao"></a>Relation.Table プロパティ (DAO)


**適用先**: Access 2013、Office 2013

**[Relation](relation-object-dao.md)** オブジェクトの主テーブルの名前を示します。これは、 **[TableDef](connection-name-property-dao.md)** オブジェクトまたは **[QueryDef](tabledef-object-dao.md)** オブジェクトの **[Name](querydef-object-dao.md)** プロパティの設定値と同じである必要があります (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .表

*式* Relation オブジェクトを表 **す変数** 。

## <a name="remarks"></a>注釈

**Table** プロパティの設定は、コレクションにまだ追加されていない新しい **Relation** オブジェクトでは、値の取得および設定が可能で、 [**Relations**](relations-collection-dao.md) コレクションの既存の **Relation** オブジェクトでは値の取得のみ可能です。

2 つのテーブルまたはクエリのフィールド間のリレーションシップを表す **Relation** オブジェクトを定義するには、**Table** プロパティを **[ForeignTable](relation-foreigntable-property-dao.md)** プロパティと共に使用します。**Table** プロパティは、主 **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値に設定し、**ForeignTable** プロパティは、外部 (参照) **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値に設定します。**[Attributes](field-attributes-property-dao.md)** プロパティは、2 つのオブジェクト間のリレーションシップの種類を決定します。

たとえば、有効なパーツ コード (PartNo という名前のフィールド) の一覧が ValidParts テーブルに保存されているとき、OrderItem テーブルとの一対多リレーションシップを確立して、パーツ コードを OrderItem テーブルに入力する場合、ValidParts テーブルにもそのパーツ コードが既に存在している必要があるようにできます。パーツ コードが ValidParts テーブルに存在しておらず、 **Relation** オブジェクトの **Attributes** プロパティを **dbRelationDontEnforce** に設定していない場合は、トラップ可能なエラーが発生します。

この例では、ValidParts テーブルが主テーブルになるため、 **Relation** オブジェクトの **Table** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **ForeignTable** プロパティが OrderItem に設定されます。 Relation **オブジェクト** の Fields コレクション内の **[Field](field-object-dao.md)** オブジェクトの Name プロパティと **ForeignName** プロパティは **[、PartNo](fields-collection-dao.md)** に設定されます。 

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
