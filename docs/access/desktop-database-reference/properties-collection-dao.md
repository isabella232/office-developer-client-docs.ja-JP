---
title: Properties コレクション (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c7dd26ac4a150ca5daa2b0011ac9373e662f2dbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622075"
---
# <a name="properties-collection-dao"></a>Properties コレクション (DAO)

**適用先**: Access 2013、Office 2013

**Properties** コレクションには、オブジェクトの特定のインスタンスのすべての **[Property](property-object-dao.md)** オブジェクトが含まれます。

## <a name="remarks"></a>注釈

**Connection** オブジェクトと **Error** オブジェクトを除くすべての DAO オブジェクトには、 **Properties** コレクションがあり、特定の組み込み **Property** オブジェクトが含まれます。この **Property** オブジェクトは、通常は単にプロパティと呼ばれ、オブジェクトのそれぞれのインスタンスの特徴を一意に指定します。

組み込みプロパティの他に、ユーザー定義のプロパティを独自に作成して追加することもできます。既存のオブジェクトのインスタンスにユーザー定義のプロパティを追加するには、 **CreateProperty** メソッドを使用して内容を定義してから **Append** メソッドを使用してコレクションに追加します。 **Properties** コレクションに追加されていないユーザー定義の **Property** オブジェクトを参照したり、ユーザー定義の **Property** オブジェクトが含まれる **Properties** コレクションに、そのオブジェクトと同じ名前の **Property** オブジェクトを追加したりしようとすると、エラーが発生します。

ユーザー定義のプロパティは **Delete** メソッドを使用して **Properties** コレクションから削除できますが、組み込みプロパティは削除できません。

> [!NOTE]
> [!メモ] ユーザー定義の **Property** オブジェクトは、1 つのオブジェクトの特定のインスタンスにのみ関連付けられます。プロパティは、選択した種類のオブジェクトのすべてのインスタンスに定義されるわけではありません。

コレクション内の組み込み **Property** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- オブジェクト。**プロパティ**(0)

- オブジェクト。**プロパティ**("name")

- オブジェクト。 \! プロパティ \[name\]

組み込みプロパティの場合、次の構文を使用することもできます。

- object.name

> [!NOTE]
> ユーザー定義プロパティの場合は、完全なオブジェクトを使用する必要があります。**プロパティ**("name") 構文。

同じ構文を使って、 **Property** オブジェクトの **Value** プロパティを参照することもできます。 **Property** オブジェクト自身と **Property** オブジェクトの **Value** プロパティのいずれを参照するかは、参照のコンテキストで決まります。

## <a name="example"></a>例

この例では、カレント データベースでユーザー定義のプロパティを作成し、 **Type** プロパティと **Value** プロパティを設定してデータベースの **Properties** コレクションに追加します。次に、データベースのすべてのプロパティを列挙します。

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

この例では、ユーザー定義のプロパティに値を設定します。プロパティが存在しない場合は、 **CreateProperty** メソッドを使用して作成してから値を設定します。このプロシージャを実行するには、SetProperty プロシージャが必要です。

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
