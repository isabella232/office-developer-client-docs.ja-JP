---
title: データを保持する (デスクトップ データベース参照のアクセス)
TOCTitle: Persisting Data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fdac02c2293088c60c3346b333b6619777b9a18
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862913"
---
# <a name="persisting-data"></a>データの永続化


**適用されます**Access 2013 |。Office 2013

ポータブル コンピューター (ラップトップなど) の場合、接続状態と切断状態の両方で実行できるアプリケーションが必要です。ADO では、クライアント カーソル **Recordset** をディスクに保存し、後で再読み込みできる機能を開発者に提供することで、このような状況をサポートしています。

複数の状況で、このような機能を使用できます。次に例を示します。

- **出張** 出張中にアプリケーションを使用する場合、後でデータベースに再接続してコミットできるように、変更および新規レコードの追加を実行できる機能を提供することが重要です。

- **更新頻度の低い参照** アプリケーションでは通常、テーブル (州税テーブルなど) は検索用に使用されます。これらのテーブルは更新頻度が低く、読み取り専用です。アプリケーションを起動するたびにこのデータをサーバーから再読み取りする代わりに、アプリケーションは単にローカルに保存された **Recordset** からデータを読み込むことができます。

ADO で **Recordset** の保存および読み込みを行うには、ADO **Recordset** オブジェクトの **Recordset.Save** メソッドおよび **Recordset.Open(,,,,adCmdFile)** メソッドを使用します。

**Recordset** **Save** メソッドを使用して、ADO **Recordset** をディスクのファイルに保存できます ( **Recordset** を ADO **Stream** オブジェクトに保存することもできます。 **Stream** オブジェクトについては、このマニュアル内で後述します)。後で、 **Recordset** を使用する準備ができたときに **Open** メソッドを使用してこれを再び開くことができます。既定では、ADO は **Recordset** を Microsoft 独自の Advanced Data TableGram (ADTG) 形式で保存します。このバイナリ形式は、 **adPersistADTG** **PersistFormatEnum** 値を使用して指定されます。代わりに **adPersistXML** を使用して、 **Recordset** を XML として保存することもできます。Recordset を XML として保存する方法の詳細については、「 [レコードを XML 形式で保存する](persisting-records-in-xml-format.md)」を参照してください。

**Save** メソッドの構文を次に示します。

`recordset.Save Destination, PersistFormat`

**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。

初めて保存した後に、続けて **Save** メソッドを呼び出すときは、*Destination* を指定すると、実行時エラーが発生するため、指定しないでください。**Save** メソッドを続けて呼び出すときに新しい *Destination* を指定すると、**Recordset** は新しい保存先に保存されます。ただし、その場合、新しい保存先と元の保存先の両方が開いています。

**Save** メソッドは、**Recordset** も *Destination* も閉じないため、**Recordset** の操作を続行し、最新の変更を保存できます。**Recordset** を閉じるまで、*Destination* は開いたままになり、その間、他のアプリケーションからその *Destination* に対する読み取りは可能ですが、書き込みはできません。

セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の場合のみ、使用が許可されます。セキュリティに関する問題の詳細については、MDAC の ActiveX データ オブジェクト (ADO) についての技術記事で、Microsoft Internet Explorer での ADO および RDS の セキュリティに関するトピックを参照してください。

非同期の **Recordset** のフェッチ、実行、または更新の操作進行中に **Save** メソッドが呼び出された場合、 **Save** メソッドは非同期操作が完了するまで待機します。

レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行に移動します。

最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。

**CursorLocation** プロパティを **adUseServer** に設定して **Recordset** を保存する場合、その **Recordset** の更新機能は制限されます。プロバイダーの機能によって異なりますが、通常は単一テーブルに対する更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも使用できません。

*Destination*パラメーターには、OLE DB **IStream**インターフェイスをサポートする任意のオブジェクトを使用できますが、あるために、ASP**応答**オブジェクトに直接**レコード セット**を保存できます。

次の例では、 **Save** メソッドと **Open** メソッドを使用して **Recordset** を保存し、後で再び開きます。

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

このセクションには、次のトピックが含まれています。

- [レコードセットの保存の詳細](more-about-recordset-persistence.md)

- [フィルター適用済みの階層 Recordset を保存する](persisting-filtered-and-hierarchical-recordsets.md)

- [レコードを XML 形式で保存する (ADO)](persisting-records-in-xml-format.md)