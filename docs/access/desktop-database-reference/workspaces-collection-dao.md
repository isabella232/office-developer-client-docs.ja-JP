---
title: Workspaces コレクション (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6f95c44eb5517ebbd0d963058123c07717be2699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588547"
---
# <a name="workspaces-collection-dao"></a>Workspaces コレクション (DAO)


**適用先**: Access 2013、Office 2013

**Workspaces** コレクションには、 **DBEngine** オブジェクトの、表示されているアクティブなすべての **Workspace** オブジェクトが含まれます。非表示の **Workspace** オブジェクトはコレクションに追加されず、割り当てられている変数によって参照されます。

## <a name="remarks"></a>注釈

**Workspace** オブジェクトを使用して、現在のセッションを管理するか別のセッションを開始します。

**Workspace** オブジェクトを初めて参照または使用すると、自動的に既定のワークスペース DBEngine.Workspaces(0) が作成されます。 この既定のワークスペースの **Name** プロパティと **UserName** プロパティの設定は、"\#Default Workspace\#" と "Admin" です。 セキュリティが有効になっている場合、 **UserName** プロパティの設定はログオンしたユーザーの名前になります。

[**CreateWorkspace**](dbengine-createworkspace-method-dao.md) メソッドを使用すると、新しい **Workspace** オブジェクトを作成できます。新しい **Workspace** オブジェクトを作成した後、それを **Workspaces** コレクションから参照する必要がある場合は、オブジェクトを **Workspaces** コレクションに追加する必要があります。ただし、新しく作成した **Workspace** オブジェクトは、 **Workspaces** コレクションに追加せずに使用することもできます。

コレクション内の **Workspace** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

**DBEngine**.**Workspaces**(0)

**DBEngine**.**Workspaces**("name")

**DBEngine**.**Workspaces**\!\[name\]


> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。



## <a name="example"></a>例

この例では、新しい Microsoft Access ワークスペース オブジェクトを作成し、 **Workspaces** コレクションに追加します。次に、 **Workspaces** コレクションおよび **Workspace** オブジェクトの **Properties** コレクションを列挙します。

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

この例では、 **CreateWorkspace** メソッドを使用して、Microsoft Access ワークスペースを作成します。次に、そのワークスペースのプロパティの一覧を表示します。

```vb 
Sub CreateWorkspaceX() 
 
 Dim wrkAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 
 DefaultType = dbUseJet 
 ' Create an unnamed Workspace object of the type 
 ' specified by the DefaultType property of DBEngine 
 ' (dbUseJet). 
 Set wrkAcc = CreateWorkspace("", "admin", "") 
 
 ' Enumerate Workspaces collection. 
 Debug.Print "Workspace objects in Workspaces collection:" 
 For Each wrkLoop In Workspaces 
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

