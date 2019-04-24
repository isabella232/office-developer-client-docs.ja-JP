---
title: Workspace メソッド (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c143d91c3dfe786c3245c2b67768c57379869e75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302549"
---
# <a name="workspacebegintrans-method-dao"></a>Workspace メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しいトランザクションを開始します。値の取得および設定が可能です。データベース型 (**Database**) の値を使用します。

## <a name="syntax"></a>構文

*式*。BeginTrans

*式***Workspace**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

トランザクション メソッドである **BeginTrans**、 **CommitTrans**、および **Rollback** は、 **Workspace** オブジェクトで定義されるセッションの間に行われるトランザクション処理を管理します。これらのメソッドは、1 セッションの間にデータベースに対して行われる一連の変更を 1 つの単位として扱う場合に、 **Workspace** オブジェクトで使用します。

通常、トランザクションは、複数のテーブル内のレコードを更新し、すべてのテーブルで変更を確実に完了 (コミット) するか、すべてのテーブルで変更を取り消す (ロールバックする) 必要がある場合に、データの整合性を維持するために使用します。たとえば、ある口座から別の口座にある金額を移す必要がある場合、一方の口座からその金額を引き、もう一方の口座にその金額を足します。いずれかの更新が失敗すると、口座の残高が合わなくなります。最初のレコードを更新する前には **BeginTrans** メソッドを使用し、以降の更新が失敗した場合は **Rollback** メソッドを使用してすべての更新を元に戻すことができます。最後のレコードを正しく更新できたら **CommitTrans** メソッドを使用します。

> [!NOTE]
> [!メモ] 1 つの **Workspace** オブジェクトでは、トランザクションは常に **Workspace** 全体に対して実行され、1 つの **Connection** オブジェクトまたは **Database** オブジェクトのみに制限されることはありません。 **Workspace** トランザクション内で複数の接続またはデータベースに対して操作を実行した場合、そのトランザクションを解決 (つまり **CommitTrans** メソッドまたは **Rollback** メソッドを使用) すると、そのワークスペース内のすべての接続およびデータベースに対するすべての操作に影響が及びます。

**CommitTrans** を使用した後は、そのトランザクション中に行った変更を取り消すことはできません (トランザクションが別のトランザクションにネストされていて、ネストしているトランザクション自体がロールバックされる場合を除く)。トランザクションをネストする場合は、現在のトランザクションを解決しない限り、ネスト内でそのトランザクションより上のレベルにあるトランザクションを解決できません。

複数のトランザクションのスコープが重複しており、ネストしていない場合に、それらのトランザクションを同時実行する場合は、別の **Workspace** オブジェクトを作成して、そのオブジェクトで同時トランザクションを実行できます。

保留中のトランザクションを解決せずに **Workspace** オブジェクトを閉じると、それらのトランザクションは自動的にロールバックされます。

先に **BeginTrans** メソッドを使用せずに **CommitTrans** メソッドまたは **Rollback** メソッドを使用すると、エラーが発生します。

Microsoft Access ワークスペースで使用される一部の ISAM データベースでは、トランザクションがサポートされておらず、この場合 **Database** オブジェクトまたは **Recordset** オブジェクトの **Transactions** プロパティは **False** です。 データベースでトランザクションがサポートされているかどうか確認するには、 **BeginTrans** メソッドを使用する前に **Database** オブジェクトの **Transactions** プロパティを調べます。 複数のデータベースを基にした **Recordset** オブジェクトを使用する場合は、 **Recordset** オブジェクトの **Transactions** プロパティを調べます。 

**Recordset** 全体が Microsoft Access データベース エンジンのテーブルを基にしている場合は、常にトランザクションを使用できます。 しかし、他のデータベース製品によって作成されたテーブルを基にした **Recordset** オブジェクトでは、トランザクションがサポートされていない場合があります。 たとえば、Paradox のテーブルを基にした **Recordset** ではトランザクションを使用できません。 この場合、 **Transactions** プロパティは **False** です。 **Database** または **Recordset** でトランザクションがサポートされていない場合、トランザクション メソッドは無視され、エラーは発生しません。

ODBC データ ソースに Microsoft Access データベース エンジンを通じてアクセスする場合は、トランザクションをネストできません。

ODBC ワークスペースでは、 **CommitTrans** を使用すると、カーソルが無効になる場合があります。 **Recordset** 内の変更を確認するには、 **Requery** メソッドを使用するか、 **Recordset** を閉じて再度開いてください。

> [!NOTE]
> - 多くの場合、ディスクへのアクセスが必要な操作をトランザクション ブロックとして分離することにより、アプリケーションのパフォーマンスを改善できます。これにより、操作をバッファーに格納できるため、ディスクへのアクセス回数を大幅に削減できる可能性があります。
> - Microsoft Access ワークスペースでは、ワークステーション上の環境変数 TEMP で指定されたディレクトリに保存されたファイルに、トランザクションがログ出力されます。トランザクション ログ ファイルによって TEMP ドライブ上の記憶領域が使い果たされてしまった場合は、データベース エンジンで実行時エラーが発生します。この時点で **CommitTrans** を使用すると、コミットされる操作の数を特定できず、その他の完了していない操作が失われるため、操作を再度実行する必要があります。 **Rollback** メソッドを使用すると、トランザクション ログが解放され、トランザクション内のすべての操作がロールバックされます。
> - 確定していないトランザクション内で複製の **Recordset** を閉じると、暗黙の **Rollback** 操作が発生します。

## <a name="example"></a>例

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
