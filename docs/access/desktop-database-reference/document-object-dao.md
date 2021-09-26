---
title: Document オブジェクト (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e7e4592d589c5039ff834106614d9ea45a26f3c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618190"
---
# <a name="document-object-dao"></a>Document オブジェクト (DAO)

**適用先**: Access 2013、Office 2013

**Document** オブジェクトには、オブジェクトの 1 つのインスタンスの情報があります。オブジェクトは、データベース、保存されたテーブル、クエリ、またはリレーションシップのいずれかです (Microsoft Access データベース エンジン データベースのみ)。

## <a name="remarks"></a>注釈

各 **Container** オブジェクトには、 **Container** オブジェクトで指定された組み込みのオブジェクトのインスタンスを記述する **Document** オブジェクトを含む **Documents** コレクションがあります。次の表に、各 **Document** オブジェクトが記述するオブジェクトの種類、その **Container** オブジェクトの名前、および **Document** オブジェクトに格納されている情報の種類を示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Document</p></th>
<th><p>コンテナー</p></th>
<th><p>格納されている情報</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>データベース</p></td>
<td><p>データベース</p></td>
<td><p>保存されたデータベース</p></td>
</tr>
<tr class="even">
<td><p>テーブルまたはクエリ</p></td>
<td><p>テーブル</p></td>
<td><p>保存されたテーブルまたはクエリ</p></td>
</tr>
<tr class="odd">
<td><p>リレーションシップ</p></td>
<td><p>Relations</p></td>
<td><p>保存されたリレーションシップ</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] 上記の表の **Container** オブジェクトと、同じ名前のコレクションを混同しないでください。Databases の **Container** オブジェクトは、保存されたすべてのデータベース オブジェクトを参照しますが、 **Databases** コレクションは、特定のワークスペースで開いているデータベース オブジェクトのみを参照します。

**Document** オブジェクトを使用すると、以下の操作を実行できます。

- **Name** プロパティを使用して、ユーザーまたは Microsoft Access データベース エンジンがオブジェクトの作成時に付けた名前を取得します。

- **Container** プロパティを使用して、 **Document** オブジェクトを含む **Container** オブジェクトの名前を取得します。

- **Owner** プロパティを使用して、オブジェクトの所有者を設定または取得します。 **Owner** プロパティを設定するには、 **Document** オブジェクトに対する書き込み権限が必要であり、プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。

- **UserName** プロパティまたは **Permissions** プロパティを使用して、オブジェクトのユーザーまたはグループのアクセス権限を設定または取得します。これらのプロパティを設定するには、 **Document** オブジェクトへの書き込み権限が必要であり、 **UserName** プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。

- **DateCreated** プロパティを使用して、 **Document** オブジェクトが作成された日時を取得し、 **LastUpdated** プロパティを使用して、最後に変更された日時を取得します。

各 **Document** オブジェクトは、既存のオブジェクトに対応しているため、 **Document** オブジェクトを新規作成したり、既存のオブジェクトを削除することはできません。コレクション内の **Document** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **Documents**(0)

- **ドキュメント**("*名*")

-  \! ドキュメント \[*name*\]

## <a name="example"></a>例

この例では、Tables コンテナーの **Documents** コレクションを列挙し、次にコレクションの最初の **Document** オブジェクトの **Properties** コレクションを列挙します。

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

次の使用例は、 **Owner** プロパティおよび **SystemDB** プロパティを使用して、さまざまな **Document** オブジェクトの所有者を表示します。

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

