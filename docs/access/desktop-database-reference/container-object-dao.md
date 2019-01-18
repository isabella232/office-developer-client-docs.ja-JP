---
title: コンテナー オブジェクト (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702125"
---
# <a name="container-object-dao"></a>コンテナー オブジェクト (DAO)

**適用されます**Access 2013、Office 2013。

**Container** オブジェクトは、同じような種類の **Document** オブジェクトを 1 つにグループ化します。

## <a name="remarks"></a>注釈

各 **Database** オブジェクトには、組み込みの **Container** オブジェクトで構成される 1 つの **Containers** コレクションがあります。アプリケーションでは、独自のドキュメントの種類とそれに対応するコンテナーを定義できますが (Microsoft Access データベース エンジンのデータベースのみ)、これらのオブジェクトが DAO でサポートされているとは限りません。

これらの **Container** オブジェクトには、Microsoft Access データベース エンジンで定義されているものもあれば、他のアプリケーションで定義されているものもあります。次の表では、Microsoft Access データベース エンジンで定義されている各 **Container** オブジェクトの名前と、そこに含まれる情報の種類を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Container の名前</p></th>
<th><p>含まれる情報の内容</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Databases</p></td>
<td><p>保存されたデータベース</p></td>
</tr>
<tr class="even">
<td><p>Tables</p></td>
<td><p>保存されたテーブルおよびクエリ</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>保存されたリレーションシップ</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] 上記の表の **Container** オブジェクトと、同じ名前のコレクションを混同しないでください。Databases の **Container** オブジェクトは、保存されたすべてのデータベース オブジェクトを参照しますが、 **Databases** コレクションは、特定のワークスペースで開いているデータベース オブジェクトのみを参照します。

各 **Container** オブジェクトには、 **Container** オブジェクトで指定された組み込みのオブジェクトのインスタンスを記述する **Document** オブジェクトを含む **Documents** コレクションがあります。 **Container** オブジェクトは、通常、 **Document** オブジェクトに含まれる情報への仲介リンクとして使用します。また、 **Containers** コレクションを使用して、任意の種類のすべての **Document** オブジェクトにセキュリティを設定することもできます。

既存の **Container** オブジェクトを使用すると、以下の操作を実行できます。

- **Name** プロパティを使用して、 **Container** オブジェクトのあらかじめ定義された名前を取得します。

- **Owner** プロパティを使用して、 **Container** オブジェクトの所有者を設定または取得します。 **Owner** プロパティを設定するには、 **Container** オブジェクトに対する権限が必要であり、プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。

- **Permissions** プロパティおよび **UserName** プロパティを使用して、 **Container** オブジェクトに対するアクセス許可を設定し、これらのアクセス許可設定が、 **Container** オブジェクトの **Documents** コレクション内に作成されるすべての **Document** オブジェクトに継承されます。

**Container** オブジェクトは組み込みのオブジェクトであるため、 **Container** オブジェクトを新規作成したり、既存のオブジェクトを削除することはできません

コレクション内の **Container** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- **Containers**(0)

- **コンテナー**(以下「*名前*」)

- **コンテナー**\!\[*名*\]

## <a name="example"></a>例

次の使用例は、Northwind データベースの **Containers** コレクション、およびコレクションに含まれる各 **Container** オブジェクトの **Properties** コレクションを列挙します。

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
