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
ms.localizationpriority: medium
ms.openlocfilehash: 45428f15c0bca259703e0f95fb7ad8693d841044
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615341"
---
# <a name="indexunique-property-dao"></a>Index.Unique プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Index](index-object-dao.md)** オブジェクトがテーブルの固有 (キー) インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .一意

*式* Index オブジェクトを表す **変数** 。

## <a name="remarks"></a>注釈

このプロパティの設定は、オブジェクトがコレクションに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。

固有インデックスは、固有の定義済み順序で、テーブル内のすべてのレコードを論理的に配列する 1 つ以上のフィールドで構成されます。固有インデックスが 1 つのフィールドで構成される場合は、そのフィールド内の値はテーブル全体で一意である必要があります。固有インデックスが複数のフィールドで構成される場合は、各フィールドでは値の重複が許されますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。

**Index** オブジェクトの **Unique** プロパティと **[Primary](index-primary-property-dao.md)** プロパティの両方が **True** に設定されている場合、そのインデックスは、固有の主インデックスとなり、定義済みの論理的な順序でテーブル内のすべてのレコードを一意に識別します。**Primary** プロパティが **False** に設定されている場合、2 次インデックスとなります。2 次インデックス (キーと非キーの両方) は、テーブル内のレコードの識別子としては機能せずに、定義済み順序でレコードを論理的に配列します。

> [!NOTE]
> - テーブルにインデックスを作成する必要はありませんが、テーブルが大きくてインデックスが設定されていない場合、特定のレコードへのアクセス時間が長くなる可能性があります。
> - インデックスのないテーブルからレコードを取得する場合、特定の順序でレコードを取得することはできません。
> - **Index** **[オブジェクト](field-attributes-property-dao.md)** 内の **[各 Field](field-object-dao.md)** オブジェクトの Attributes プロパティは、レコードの順序を決定し、その Index オブジェクトに使用するアクセス手法 **を決定** します。
> - 固有インデックスは、レコードの検索を最適化するのに便利です。
> - インデックスは、基本テーブルの物理的な順序には影響を与えかねない。インデックスは、特定のインデックスが選択されている場合、または Microsoft Access データベース エンジンが Recordset オブジェクトを作成するときに、テーブル型 **[Recordset](recordset-object-dao.md)** オブジェクトによってレコードがどのようにアクセスされるのかにのみ **影響** します。

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
