---
title: ワークスぺース コレクション (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c615be9e92a936486c15377514c2b695f68bb5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698415"
---
# <a name="workspaces-collection-dao"></a>ワークスぺース コレクション (DAO)


**適用されます**Access 2013、Office 2013。

**Workspaces** コレクションには、 **DBEngine** オブジェクトの、表示されているアクティブなすべての **Workspace** オブジェクトが含まれます。非表示の **Workspace** オブジェクトはコレクションに追加されず、割り当てられている変数によって参照されます。

## <a name="remarks"></a>注釈

**Workspace** オブジェクトを使用して、現在のセッションを管理するか別のセッションを開始します。

最初を参照してくださいか、**ワークスペース**オブジェクトを使用して、DBEngine.Workspaces(0)、既定のワークスペースを自動的に作成します。 既定のワークスペースの**名前**と**ユーザー名**のプロパティの設定は、"\#既定のワークスぺース\#」と「Admin」に、それぞれ。 セキュリティが有効になっている場合、 **UserName** プロパティの設定はログオンしたユーザーの名前になります。

[**CreateWorkspace**](dbengine-createworkspace-method-dao.md) メソッドを使用すると、新しい **Workspace** オブジェクトを作成できます。新しい **Workspace** オブジェクトを作成した後、それを **Workspaces** コレクションから参照する必要がある場合は、オブジェクトを **Workspaces** コレクションに追加する必要があります。ただし、新しく作成した **Workspace** オブジェクトは、 **Workspaces** コレクションに追加せずに使用することもできます。

コレクション内の **Workspace** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

**DBEngine**。**ワークスペース**(0)

**DBEngine**。**ワークスペース**("name")

**DBEngine**。**ワークスペース**\!\[名\]


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

