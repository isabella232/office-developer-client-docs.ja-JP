---
title: Index.Primary プロパティ (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff99f60fce41c7fa7de604a5109e68f6f744e68a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997645"
---
# <a name="indexprimary-property-dao"></a>Index.Primary プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

**[Index](index-object-dao.md)** オブジェクトがテーブルの主キー インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。プライマリ

*式***Index**オブジェクトを表す変数です。

## <a name="remarks"></a>解説

**Primary** プロパティの設定は、新しい **Index** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Indexes**](indexes-collection-dao.md) コレクション内の既存の **Index** オブジェクトの場合は値の取得のみ可能です。 **Index** オブジェクトが **[TableDef](tabledef-object-dao.md)** オブジェクトに追加されていても、 **TableDef** オブジェクトが **[TableDefs](tabledefs-collection-dao.md)** コレクションに追加されていない場合、 **Index** プロパティは値の取得および設定が可能です。

主キー インデックスは、定義済みの順序で、テーブル内のすべてのレコードを一意に識別する 1 つ以上のフィールドで構成されます。インデックス フィールドは一意にする必要があるため、 [Index](index-unique-property-dao.md) オブジェクトの ****Unique**** プロパティを **True** に設定します。主キー インデックスが複数のフィールドで構成される場合、それぞれのフィールドには重複する値を格納できますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。主キー インデックスはテーブルのキーで構成され、通常、主キーと同じフィールドが含まれます。

> [!NOTE]
> [!メモ] 必ずしもテーブルにインデックスを作成する必要はありませんが、インデックスを持たない大きなテーブルでは、特定のレコードにアクセスするのに長い時間がかかる場合があります。 [Index](field-attributes-property-dao.md) オブジェクト内にある各 [**Field**](field-object-dao.md) オブジェクトの ****Attributes**** プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。データベースに新しいテーブルを作成する場合は、各レコードが一意に識別される 1 つ以上のフィールドでインデックスを作成し、 **Index** オブジェクトの **Primary** プロパティを **True** に設定することをお勧めします。

テーブルの主キーを設定すると、その主キーがテーブルの主キー インデックスとして自動的に定義されます。

## <a name="example"></a>例

この例では、 **Primary** プロパティを使用して、新しい **TableDef** オブジェクトの新しい **定数** オブジェクトをそのテーブルの主 **Index** オブジェクトとして指定します。 **Primary** プロパティを **True** に設定すると、 **Unique** プロパティおよび **Required** プロパティも自動的に **True** に設定されます。

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
