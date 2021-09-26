---
title: Workspace オブジェクト (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: d6f676033c5619915f15605eababaaf7aaeb01c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588566"
---
# <a name="workspace-object-dao"></a>Workspace オブジェクト (DAO)

**適用先**: Access 2013、Office 2013

**Workspace** オブジェクトは、ユーザー用に名前付きセッションを定義します。これには開いているデータベースが含まれ、同時実行トランザクションのメカニズムを提供し、Microsoft Access ワークスペースの場合は、セキュリティが設定されたワークグループをサポートします。

## <a name="remarks"></a>注釈

**Workspace** オブジェクトは、アプリケーションが Microsoft Access データベース エンジンを使用してデータを操作する方法を定義する非永続的なオブジェクトです。現在のセッションの管理、または追加のセッションの開始に、 **Workspace** オブジェクトを使用します。セッションでは、複数のデータベースまたは接続を開き、トランザクションを管理できます。たとえば、以下の操作を実行できます。

- **Name** 、 **UserName** 、および **Type** の各プロパティを使用して、名前付きセッションを確立します。セッションでは、複数のデータベースを開き、ネストされたトランザクションの 1 つのインスタンスを実行できる適用範囲が作成されます。

- **Close** メソッドを使用して、セッションを終了します。

- **OpenDatabase** メソッドを使用して、 **Workspace** で 1 つまたは複数の既存のデータベースを開きます。

- **BeginTrans** 、 **CommitTrans** 、および **Rollback** の各メソッドを使用して、 **Workspace** 内のネストされたトランザクションの処理を管理し、複数の **Workspace** オブジェクトを使用して、複数のトランザクション、同時実行トランザクション、および重なり合うトランザクションを実行します。

**Workspace** オブジェクトを初めて参照または使用すると、自動的に既定のワークスペース DBEngine.Workspaces(0) が作成されます。この既定のワークスペースの **Name** プロパティと **UserName** プロパティの設定は、"\#Default Workspace\#" と "Admin" です。セキュリティが有効になっている場合、**UserName** プロパティの設定はログオンしたユーザーの名前になります。

トランザクションを使用する場合、 **Workspace** オブジェクトで複数の **Database** オブジェクトが開かれていると、指定した **Workspace** オブジェクトのすべてのデータベースが影響を受けます。たとえば、 **BeginTrans** メソッドを使用し、あるデータベースの複数のレコードを更新した後、別のデータベースのレコードを削除します。次に、 **Rollback** メソッドを使用すると、更新と削除の両方の操作がキャンセルされ、ロールバックされます。複数の **Database** オブジェクトにまたがってトランザクションを個別に管理するには、追加の **Workspace** オブジェクトを作成します。

**CreateWorkspace** メソッドを使用して、 **Workspace** オブジェクトを作成できます。新しい **Workspace** オブジェクトを作成した後、それを **Workspaces** コレクションから参照する必要がある場合は、オブジェクトを **Workspaces** コレクションに追加する必要があります。

新規に作成された **Workspace** オブジェクトは、 **Workspaces** コレクションに追加しなくても使用できます。ただし、オブジェクトに割り当てたオブジェクト変数で参照する必要があります。

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
            If prpLoop <> "" Then Debug.Print "  " & _ 
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
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

次の例は、DAO (Data Access Objects) ワークスペース内でトランザクションを使用する方法を示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
