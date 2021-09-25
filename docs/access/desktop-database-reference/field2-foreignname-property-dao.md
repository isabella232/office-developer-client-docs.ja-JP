---
title: Field2.ForeignName プロパティ (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: f0cda5a100aadea71600ea6f21f6eac178870982
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577354"
---
# <a name="field2foreignname-property-dao"></a>Field2.ForeignName プロパティ (DAO)


**適用先:** Access 2013、Office 2013

あるリレーションシップにおいて、主テーブルのフィールドに対応する外部キー側のテーブルの **Field2** オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .ForeignName

*式***Field2** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**[Relation](relation-object-dao.md)** オブジェクトが **[Database](database-object-dao.md)** に追加されていない状態で、 **Field2** オブジェクトを **Relation** オブジェクトに追加する場合は、 **ForeignName** プロパティは値の取得および設定が可能です。 **Relation** オブジェクトがデータベースに追加されると、 **ForeignName** プロパティは値の取得のみが可能になります。

**ForeignName** プロパティをサポートできるのは、 **Relation** オブジェクトの **Fields** コレクションに属している **Field2** オブジェクトのみです。

**Field2** **[オブジェクト](connection-name-property-dao.md)** の Name プロパティと **ForeignName** プロパティ設定では、リレーションシップのプライマリ テーブルと外部テーブルの対応するフィールドの名前を指定します。 **[Relation オブジェクトの](relation-table-property-dao.md)** Table プロパティ **[と ForeignTable](relation-foreigntable-property-dao.md)** プロパティの設定によって、リレーションシップのプライマリ テーブルと外部テーブルが決定されます。 

たとえば、ValidParts テーブルに有効な部品コード (PartNo という名前のフィールド) の一覧が格納されている場合、OrderItem テーブルに部品コードが入力されるときには、その部品コードが ValidParts テーブルに既に存在している必要があるという、OrderItem テーブルとのリレーションシップを設定できます。 パーツ コードが ValidParts テーブルに存在しない場合 **、Relation** オブジェクトの **[Attributes](field-attributes-property-dao.md)** プロパティを **dbRelationDontEnforce** に設定していない場合は、トラップ可能なエラーが発生します。

この場合は、ValidParts テーブルが外部キー側のテーブルであるため、 **Relation** オブジェクトの **ForeignTable** プロパティは ValidParts に設定され、 **Relation** オブジェクトの **Table** プロパティは OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクションに含まれる **Field2** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。

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
