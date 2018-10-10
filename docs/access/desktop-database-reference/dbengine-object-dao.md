---
title: DBEngine オブジェクト (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc2889ad38bdc95316735901b25314f26d8df754
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479105"
---
# <a name="dbengine-object-dao"></a>DBEngine オブジェクト (DAO)

**適用されます**Access 2013 |。Office 2013

**DBEngine** オブジェクトは、DAO オブジェクト モデル内のトップ レベル オブジェクトです。

## <a name="remarks"></a>解説

**DBEngine** オブジェクトは、DAO オブジェクトの階層内にあるその他のすべてのオブジェクトを含み、制御を行います。追加の **DBEngine** オブジェクトの作成はできず、 **DBEngine** オブジェクトはコレクションの要素ではありません。

いずれのデータベースまたは接続を使用しても、以下の操作を実行できます。

  - **Version** プロパティを使用して、DAO バージョン番号を取得します。

  - **LoginTimeout** プロパティを使用して、ODBC ログイン タイムアウトを取得または設定し、 **RegisterDatabase** メソッドを使用して、Microsoft Access データベース エンジンに ODBC 情報を提供します。

  - **DefaultPassword** プロパティおよび **DefaultUser** プロパティを使用して、既定の **Workspace** オブジェクトのユーザー ID とパスワードを設定します。

  - **CreateWorkspace** メソッドを使用して、新しい **Workspace** オブジェクトを作成します。オプションの引数を使用すると、 **DefaultType** 、 **DefaultPassword** 、および **DefaultUser** の各プロパティの設定を無効にできます。

  - **OpenDatabase** メソッドを使用して、既定の **Workspace** 内のデータベースを開き、 **BeginTrans** 、 **Commit** 、および **Rollback** の各メソッドを使用して、既定の **Workspace** オブジェクト上のトランザクションを制御します。

  - **Workspaces** コレクションを使用して、特定の **Workspace** オブジェクトを参照します。

  - **Errors** コレクションを使用して、データ アクセス エラーの詳細を調べます。

その他のプロパティとメソッドは、DAO と Microsoft Access データベース エンジンを組み合わせて使用する場合のみ使用できます。この組み合わせを使用すると、Microsoft Access データベース エンジンの制御、そのプロパティの操作、およびコレクションの要素ではない一時オブジェクトに対するタスクの実行が可能です。たとえば、以下の操作を実行できます。

  - **CreateDatabase** メソッドを使用して、新しい Microsoft Access データベース エンジン **Database** オブジェクトを作成します。

  - **Idle** メソッドを使用して、Microsoft Access データベース エンジンが任意の保留中タスクを完了できるようにします。

  - **CompactDatabase** メソッドおよび **RepairDatabase** メソッドを使用して、データベース ファイルを保守します。

  - **IniPath** プロパティを使用して、Microsoft Access データベース エンジンの Windows レジストリ情報の位置を指定し、 **SystemDB** プロパティを使用して、Microsoft Access ワークグループ情報ファイルの位置を指定します。 **SetOption** メソッドを使用すると、Microsoft Access データベース エンジンの Windows レジストリ設定を上書きできます。

**DefaultType** プロパティ設定および **IniPath** プロパティ設定を変更すると、これらの変更は後続の **Workspace** オブジェクトのみに反映されます。

**DBEngine** オブジェクトに属するコレクション、またはこのオブジェクトに適用されるメソッドまたはプロパティを参照するには、次の構文を使用します。

\[**DBEngine**。\]\[コレクション |メソッド。プロパティ\]

## <a name="example"></a>例

この例では、 **DBEngine** オブジェクトのコレクションを列挙します。

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
