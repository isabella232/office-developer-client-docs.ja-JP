---
title: Index.Unique プロパティ (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd3bd047afed2e547be0fb7b6999c16dd0b12cc1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996476"
---
# <a name="indexunique-property-dao"></a>Index.Unique プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

**[Index](index-object-dao.md)** オブジェクトがテーブルの固有 (キー) インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。一意

*式***Index**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

このプロパティの設定は、オブジェクトがコレクションに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。

固有インデックスは、固有の定義済み順序で、テーブル内のすべてのレコードを論理的に配列する 1 つ以上のフィールドで構成されます。固有インデックスが 1 つのフィールドで構成される場合は、そのフィールド内の値はテーブル全体で一意である必要があります。固有インデックスが複数のフィールドで構成される場合は、各フィールドでは値の重複が許されますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。

**Index** オブジェクトの [Unique](index-primary-property-dao.md) プロパティと ****Primary**** プロパティの両方が **True** に設定されている場合、そのインデックスは、固有の主インデックスとなり、定義済みの論理的な順序でテーブル内のすべてのレコードを一意に識別します。 **Primary** プロパティが **False** に設定されている場合、2 次インデックスとなります。2 次インデックス (キーと非キーの両方) は、テーブル内のレコードの識別子としては機能せずに、定義済み順序でレコードを論理的に配列します。

> [!NOTE]
> - テーブルにインデックスを作成する必要はありませんが、テーブルが大きくてインデックスが設定されていない場合、特定のレコードへのアクセス時間が長くなる可能性があります。
> - インデックスのないテーブルからレコードを取得する場合、特定の順序でレコードを取得することはできません。
> - [Index](field-attributes-property-dao.md) オブジェクト内の各 [**Field**](field-object-dao.md) オブジェクトの ****Attributes**** プロパティによって、レコードの順序が決まり、したがって該当する **Index** オブジェクトに使用するアクセス手法が決まります。
> - 固有インデックスは、レコードの検索を最適化するのに便利です。
> - インデックスはベース テーブルの物理的順序を変更しません。影響を与える方法のみレコードにアクセスするテーブル タイプの**[Recordset](recordset-object-dao.md)** オブジェクトが特定のインデックスを選択した場合、または Microsoft Access データベース エンジンは、**レコード セット**オブジェクトを作成するときにインデックスを作成します。

## <a name="example"></a>例

次の例では、新しい **Index** オブジェクトの **Unique** プロパティを **True** に設定し、Index オブジェクトを Employees テーブルの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの **Indexes** コレクションと各 **Index** オブジェクトの **Properties** コレクションを列挙します。新しい **Index** オブジェクトでは、 **TableDef** オブジェクトの Country、LastName、FirstName の特定の組み合わせを持つレコードが 1 つのみ許可されます。

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
