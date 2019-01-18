---
title: Workspace.CommitTrans メソッド (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52af229f03b7ea10510f3e580ba2c4e12784e461
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712324"
---
# <a name="workspacecommittrans-method-dao"></a>Workspace.CommitTrans メソッド (DAO)

**適用されます**Access 2013、Office 2013。

現在のトランザクションを終了し、変更を保存します。

## <a name="syntax"></a>構文

*式*です。CommitTrans (***オプション***)

*式***ワークスペース**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>Microsoft Access ワークスペースでは、 <strong>CommitTrans</strong> で定数 <strong>dbForceOSFlush</strong> を指定できます。これにより、更新を一時的にキャッシュする代わりに、すべての更新が即座にディスクにフラッシュされます。このオプションを使用しないと、アプリケーション プログラムが <strong>CommitTrans</strong> を呼び出した直後にユーザーに制御が戻り、ユーザーがコンピューターの電源が切ったためにデータがディスクに書き込まれないということが起こり得ます。このオプションを使用すると、アプリケーションのパフォーマンスに影響を与える可能性がありますが、キャッシュされた更新がディスクに保存される前にコンピューターの電源が切れる可能性がある状況においては、このオプションが役立ちます。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

トランザクションのメソッド **BeginTrans**、 **CommitTrans**、および **Rollback** は、 **Workspace** オブジェクトによって定義されたセッション中のトランザクション処理を管理します。これらのメソッドを **Workspace** オブジェクトで使用すると、1 つのセッション中にデータベースに対して行われた一連の変更を 1 つの単位として扱うことができます。

一般に、2 つ以上のテーブルのレコードを更新する必要があり、かつ変更がすべてのテーブルで完了する (コミットされる) か変更が一切行われない (ロールバックされる) ようにする必要がある場合、データの整合性を保つためにトランザクションが使用されます。たとえば、ある口座から別の口座に送金する場合は、一方の口座から金額を減らし、その金額をもう一方の口座に加算します。どちらか一方の更新が失敗すると口座の残高が合わなくなります。最初のレコードを更新する前に **BeginTrans** メソッドを使用し、以降の更新が 1 つでも失敗した場合は、 **Rollback** メソッドを使用してすべての更新を取り消すことができます。最後のレコードが正常に更新された後に **CommitTrans** メソッドを使用します。

> [!NOTE]
> [!メモ] 1 つの **Workspace** オブジェクト内では、トランザクションは **Workspace** に対して常にグローバルに適用され、1 つの **Connection** オブジェクトや **Database** オブジェクトに制限されることはありません。 **Workspace** の 1 つのトランザクション内の複数の接続またはデータベースに対して操作を実行する場合は、そのトランザクションを解決 (つまり、 **CommitTrans** メソッドまたは **Rollback** メソッドを使用) することにより、そのワークスペース内のすべての接続およびデータベースに対するすべての操作が影響を受けます。

**CommitTrans** を使用した後は、そのトランザクション中に行った変更を取り消すことはできません (トランザクションが別のトランザクションにネストされていて、ネストしているトランザクション自体がロールバックされる場合を除く)。トランザクションをネストする場合は、現在のトランザクションを解決しない限り、ネスト内でそのトランザクションより上のレベルにあるトランザクションを解決できません。

部分的に重なり、ネストしていない適用範囲を持つ同時トランザクションを定義するには、同時トランザクションを格納するための追加の **Workspace** オブジェクトを作成します。

確定していないトランザクションを解決せずに **Workspace** オブジェクトを閉じた場合、すべてのトランザクションが自動的にロールバックされます。

最初に **BeginTrans** メソッドを使用せずに **CommitTrans** メソッドまたは **Rollback** メソッドを使用すると、エラーが発生します。

Microsoft Access ワークスペースで使用される一部の ISAM データベースはトランザクションをサポートしていない場合があります ( **Database** オブジェクトまたは **Recordset** オブジェクトの **Transactions** プロパティが **False**)。 データベースでトランザクションがサポートされていることを確認するには、 **BeginTrans** メソッドを使用する前に **Database** オブジェクトの **Transactions** プロパティの値を調べます。 複数のデータベースに基づく **Recordset** オブジェクトを使用している場合は、 **Recordset** オブジェクトの **Transactions** プロパティを調べます。 

**Recordset** が Microsoft Access データベース エンジンのテーブルのみに基づいている場合は、トランザクションを使用できます。 一方、他のデータベース製品によって作成されたテーブルに基づく **Recordset** オブジェクトの場合は、トランザクションをサポートしていないことがあります。 たとえば、Paradox テーブルに基づく **Recordset** では、トランザクションを使用できません。 この場合、 **Transactions** プロパティは **False** です。 **Database** または **Recordset** がトランザクションをサポートしていない場合、メソッドは無視され、エラーは発生しません。

Microsoft Access データベース エンジンを通じて ODBC データ ソースにアクセスする場合は、トランザクションをネストできません。

ODBC ワークスペースでは、 **CommitTrans** を使用すると、カーソルが無効になることがあります。 **Requery** メソッドを使って **Recordset** 内の変更を確認するか、 **Recordset** をいったん閉じて、開き直してください。

> [!NOTE]
> - 多くの場合、ディスクへのアクセスを必要とする操作をトランザクション ブロックに分割することにより、アプリケーションのパフォーマンスを向上できます。この場合、操作がバッファーされるので、ディスクへのアクセス回数が大幅に減ります。
> - Microsoft Access ワークスペースでは、ワークステーション上の TEMP 環境変数で指定されたディレクトリ内にあるファイルに、トランザクション ログが記録されます。TEMP ドライブ上の使用可能な記憶域がトランザクション ログ ファイルによって使い尽くされた場合、実行時エラーが発生します。この時点で **CommitTrans** を使用すると、一部の操作はコミットされますが、残りの未完了の操作は失われるため、操作をやり直す必要があります。 **Rollback** メソッドを使用すると、トランザクション ログが解放され、そのトランザクション内のすべての操作がロールバックされます。
> - 確定していないトランザクション内で複製の **Recordset** を閉じると、暗黙の **Rollback** 操作が発生します。

## <a name="example"></a>例

次の例は、DAO (Data Access Objects) ワークスペース内でトランザクションを使用する方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。


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
