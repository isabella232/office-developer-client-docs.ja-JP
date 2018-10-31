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
# <a name="persisting-data"></a><span data-ttu-id="0d104-102">データの永続化</span><span class="sxs-lookup"><span data-stu-id="0d104-102">Persisting Data</span></span>


<span data-ttu-id="0d104-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d104-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d104-p101">ポータブル コンピューター (ラップトップなど) の場合、接続状態と切断状態の両方で実行できるアプリケーションが必要です。ADO では、クライアント カーソル **Recordset** をディスクに保存し、後で再読み込みできる機能を開発者に提供することで、このような状況をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0d104-p101">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state. ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="0d104-106">複数の状況で、このような機能を使用できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0d104-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="0d104-107">**出張** 出張中にアプリケーションを使用する場合、後でデータベースに再接続してコミットできるように、変更および新規レコードの追加を実行できる機能を提供することが重要です。</span><span class="sxs-lookup"><span data-stu-id="0d104-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="0d104-p102">**更新頻度の低い参照** アプリケーションでは通常、テーブル (州税テーブルなど) は検索用に使用されます。これらのテーブルは更新頻度が低く、読み取り専用です。アプリケーションを起動するたびにこのデータをサーバーから再読み取りする代わりに、アプリケーションは単にローカルに保存された **Recordset** からデータを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="0d104-p102">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables. They are infrequently updated and are read-only. Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="0d104-111">ADO で **Recordset** の保存および読み込みを行うには、ADO **Recordset** オブジェクトの **Recordset.Save** メソッドおよび **Recordset.Open(,,,,adCmdFile)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d104-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="0d104-p103">**Recordset** **Save** メソッドを使用して、ADO **Recordset** をディスクのファイルに保存できます ( **Recordset** を ADO **Stream** オブジェクトに保存することもできます。 **Stream** オブジェクトについては、このマニュアル内で後述します)。後で、 **Recordset** を使用する準備ができたときに **Open** メソッドを使用してこれを再び開くことができます。既定では、ADO は **Recordset** を Microsoft 独自の Advanced Data TableGram (ADTG) 形式で保存します。このバイナリ形式は、 **adPersistADTG** **PersistFormatEnum** 値を使用して指定されます。代わりに **adPersistXML** を使用して、 **Recordset** を XML として保存することもできます。Recordset を XML として保存する方法の詳細については、「 [レコードを XML 形式で保存する](persisting-records-in-xml-format.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d104-p103">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk. (You can also save a **Recordset** to an ADO **Stream** object. **Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it. By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format. This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value. Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**. For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="0d104-119">**Save** メソッドの構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0d104-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="0d104-p104">**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0d104-p104">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="0d104-p105">初めて保存した後に、続けて **Save** メソッドを呼び出すときは、*Destination* を指定すると、実行時エラーが発生するため、指定しないでください。**Save** メソッドを続けて呼び出すときに新しい *Destination* を指定すると、**Recordset** は新しい保存先に保存されます。ただし、その場合、新しい保存先と元の保存先の両方が開いています。</span><span class="sxs-lookup"><span data-stu-id="0d104-p105">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="0d104-p106">**Save** メソッドは、**Recordset** も *Destination* も閉じないため、**Recordset** の操作を続行し、最新の変更を保存できます。**Recordset** を閉じるまで、*Destination* は開いたままになり、その間、他のアプリケーションからその *Destination* に対する読み取りは可能ですが、書き込みはできません。</span><span class="sxs-lookup"><span data-stu-id="0d104-p106">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="0d104-p107">セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の場合のみ、使用が許可されます。セキュリティに関する問題の詳細については、MDAC の ActiveX データ オブジェクト (ADO) についての技術記事で、Microsoft Internet Explorer での ADO および RDS の セキュリティに関するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d104-p107">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="0d104-129">非同期の **Recordset** のフェッチ、実行、または更新の操作進行中に **Save** メソッドが呼び出された場合、 **Save** メソッドは非同期操作が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="0d104-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="0d104-p108">レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d104-p108">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="0d104-p109">最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="0d104-p109">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="0d104-p110">**CursorLocation** プロパティを **adUseServer** に設定して **Recordset** を保存する場合、その **Recordset** の更新機能は制限されます。プロバイダーの機能によって異なりますが、通常は単一テーブルに対する更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも使用できません。</span><span class="sxs-lookup"><span data-stu-id="0d104-p110">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="0d104-137">*Destination*パラメーターには、OLE DB **IStream**インターフェイスをサポートする任意のオブジェクトを使用できますが、あるために、ASP**応答**オブジェクトに直接**レコード セット**を保存できます。</span><span class="sxs-lookup"><span data-stu-id="0d104-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="0d104-138">次の例では、 **Save** メソッドと **Open** メソッドを使用して **Recordset** を保存し、後で再び開きます。</span><span class="sxs-lookup"><span data-stu-id="0d104-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

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

<span data-ttu-id="0d104-139">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d104-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="0d104-140">レコードセットの保存の詳細</span><span class="sxs-lookup"><span data-stu-id="0d104-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="0d104-141">フィルター適用済みの階層 Recordset を保存する</span><span class="sxs-lookup"><span data-stu-id="0d104-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="0d104-142">レコードを XML 形式で保存する (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d104-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)