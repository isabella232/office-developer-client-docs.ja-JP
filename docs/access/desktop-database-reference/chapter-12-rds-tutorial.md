---
title: '12章: リモートデータサービス (RDS) チュートリアル'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296480"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="0b506-102">12章: リモートデータサービス (RDS) チュートリアル</span><span class="sxs-lookup"><span data-stu-id="0b506-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="0b506-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b506-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b506-104">このチュートリアルでは、RDS プログラミング モデルを使用してデータ ソースのクエリおよび更新を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b506-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="0b506-105">最初に、このタスクの実行に必要な手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="0b506-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="0b506-106">このチュートリアルは、microsoft visual Basic Scripting Edition と microsoft visual J++ でも使用されています。これは、Windows Foundation Classes (ado/WFC) 用の ado を特徴としています。</span><span class="sxs-lookup"><span data-stu-id="0b506-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="0b506-107">このチュートリアルは、次の 2 つの理由から、複数の言語でコーディングされています。</span><span class="sxs-lookup"><span data-stu-id="0b506-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="0b506-p102">RDS の文書は、Visual Basic でのコーディングを前提にしています。そのため、Visual Basic のプログラマには便利ですが、他の言語を使用するプログラマには不便な場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b506-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="0b506-110">RDS の特定の機能についてわからない場合に、他の言語について多少の知識があれば、他の言語で記述された同じ機能を参照することによって問題を解決できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b506-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="0b506-p103">このチュートリアルは、RDS プログラミング モデルに基づいています。プログラミング モデルの各手順を 1 つずつ説明します。さらに、それぞれの手順に Visual Basic コードの一部を示してあります。</span><span class="sxs-lookup"><span data-stu-id="0b506-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="0b506-p104">他の言語についても、コード例を最小限の説明と共に取り上げています。各プログラム言語のチュートリアルの手順には、プログラミング モデルとチュートリアルの説明にある手順に対応する番号が付いています。この手順番号を利用して、対応するチュートリアルの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b506-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="0b506-p105">RDS プログラミング モデルについて、次に説明します。チュートリアルを使用するうえでのガイドラインとして使用してください。</span><span class="sxs-lookup"><span data-stu-id="0b506-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="0b506-119">RDS プログラミング モデルとオブジェクト</span><span class="sxs-lookup"><span data-stu-id="0b506-119">RDS programming model with objects</span></span>

- <span data-ttu-id="0b506-120">サーバーで呼び出されるプログラムを指定し、クライアントからそのプログラムを参照するための経路 (プロキシ) を取得します。</span><span class="sxs-lookup"><span data-stu-id="0b506-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="0b506-p106">サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。</span><span class="sxs-lookup"><span data-stu-id="0b506-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="0b506-p107">サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は ADO を使用して取得します。また、サーバー上で **Recordset** オブジェクトを処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b506-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="0b506-125">サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="0b506-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="0b506-126">クライアント側では、ビジュアル コントロールを使用すると、必要に応じてフォームに **Recordset** オブジェクトを簡単に配置できます。</span><span class="sxs-lookup"><span data-stu-id="0b506-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="0b506-127">**Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="0b506-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="0b506-128">手順 1: サーバープログラムを指定する</span><span class="sxs-lookup"><span data-stu-id="0b506-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="0b506-129">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span><span class="sxs-lookup"><span data-stu-id="0b506-129">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object).</span></span> <span data-ttu-id="0b506-130">サーバープログラムはサーバー上でインスタンス化され、サーバープログラム (*プロキシ*) への参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="0b506-130">A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="0b506-131">このチュートリアルでは、既定のサーバー プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b506-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="0b506-132">手順 2: サーバープログラムを呼び出す</span><span class="sxs-lookup"><span data-stu-id="0b506-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="0b506-p109">クライアントの "プロキシ" でメソッドを呼び出すと、サーバー上の実際のプログラムでメソッドが実行されます。この手順では、サーバー上でクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="0b506-p109">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="0b506-135">パート A</span><span class="sxs-lookup"><span data-stu-id="0b506-135">Part A</span></span>

<span data-ttu-id="0b506-136">このチュートリアルで rdsserver.datafactory を使用して[い](datafactory-object-rdsserver.md)ない場合は、この手順を実行する最も便利な方法は、RDS を使用することです[。DataControl](datacontrol-object-rds.md)オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0b506-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="0b506-137">**RDS.DataControl** によって、プロキシを作成する前の手順が、クエリを発行するこの手順と結合されます。</span><span class="sxs-lookup"><span data-stu-id="0b506-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="0b506-138">RDS を設定し**ます。DataControl**オブジェクト[サーバー](server-property-rds.md)のプロパティを使用して、サーバープログラムをインスタンス化する場所を識別します。</span><span class="sxs-lookup"><span data-stu-id="0b506-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="0b506-139">[connect](connect-property-rds.md)プロパティを設定して、データソースにアクセスするための接続文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b506-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="0b506-140">[SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado)プロパティを設定して、クエリコマンドテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b506-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="0b506-141">サーバープログラムがデータソースに接続し、クエリで指定された行を取得し、 **Recordset**オブジェクトをクライアントに返すようにするには、 [Refresh](refresh-method-rds.md)メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0b506-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="0b506-142">このチュートリアルでは **RDS.DataControl** を使用しませんが、使用する場合は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0b506-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="0b506-143">また、このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0b506-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="0b506-144">パート B</span><span class="sxs-lookup"><span data-stu-id="0b506-144">Part B</span></span>

<span data-ttu-id="0b506-145">この手順を実行するための一般的な方法は、 **rdsserver.datafactory**オブジェクトの[Query](query-method-rds.md)メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="0b506-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="0b506-146">このメソッドは、データ ソースへの接続に使用される接続文字列と、データ ソースから返される行の指定に使用されるコマンド テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0b506-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="0b506-147">このチュートリアルでは、 **DataFactory** オブジェクトの **Query** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b506-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="0b506-148">手順 3: サーバーが Recordset を取得する</span><span class="sxs-lookup"><span data-stu-id="0b506-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="0b506-p112">サーバー プログラムは、目的の行のデータ ソースのクエリを実行するために、接続文字列とコマンド テキストを使用します。通常、この **Recordset** の取得には ADO が使用されますが、マイクロソフトのその他のデータ アクセス インターフェイス (OLE DB など) を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b506-p112">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="0b506-151">カスタマー サーバー プログラムは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0b506-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="0b506-152">手順 4: サーバーが Recordset を返す</span><span class="sxs-lookup"><span data-stu-id="0b506-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="0b506-153">RDS は、取得した**recordset**オブジェクトを、クライアントに送り返すことができるフォームに変換します (つまり、 **recordset**を*マーシャリング*します)。</span><span class="sxs-lookup"><span data-stu-id="0b506-153">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**).</span></span> <span data-ttu-id="0b506-154">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span><span class="sxs-lookup"><span data-stu-id="0b506-154">The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library.</span></span> <span data-ttu-id="0b506-155">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span><span class="sxs-lookup"><span data-stu-id="0b506-155">However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="0b506-156">クライアント側では、 **Recordset** オブジェクトが返され、ローカル変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b506-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="0b506-157">手順 5: DataControl を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="0b506-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="0b506-p114">返された **Recordset** オブジェクトは、利用可能な状態です。他の **Recordset** と同様に、調査、移動、または編集を行うことができます。 **Recordset** に対して実行できる操作は、環境によって異なります。Visual Basic および Visual C++ には、直接的に、またはデータ コントロールを使って間接的に **Recordset** を使用できる、ビジュアル コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="0b506-p114">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="0b506-162">たとえば、Internet Explorer で web ページを表示している場合は、ビジュアルコントロールに**Recordset**オブジェクトのデータを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0b506-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="0b506-163">web ページ上のビジュアルコントロールは、 **Recordset**オブジェクトに直接アクセスできません。</span><span class="sxs-lookup"><span data-stu-id="0b506-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="0b506-164">しかし、 **DataControl (RDS)** を通じて [Recordset](datacontrol-object-rds.md) にアクセスすることはできます。</span><span class="sxs-lookup"><span data-stu-id="0b506-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="0b506-165">**RDS.DataControl** は、その [SourceRecordset](recordset-sourcerecordset-properties-rds.md) プロパティが **Recordset** オブジェクトに設定されている場合に、ビジュアル コントロールによって使用可能な状態になります。</span><span class="sxs-lookup"><span data-stu-id="0b506-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="0b506-166">ビジュアル コントロール オブジェクトの **DATASRC** パラメーターは **RDS.DataControl** に、 **DATAFLD** プロパティは **Recordset** オブジェクトのフィールド (列) に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b506-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="0b506-167">このチュートリアルでは、 **SourceRecordset** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0b506-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="0b506-168">手順 6: サーバーに変更が送信される</span><span class="sxs-lookup"><span data-stu-id="0b506-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="0b506-169">**Recordset** オブジェクトが編集された場合、あらゆる変更内容 (つまり、追加、変更、または削除された行) をサーバーに返送できます。</span><span class="sxs-lookup"><span data-stu-id="0b506-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="0b506-170">[!メモ] ADO オブジェクトおよび Microsoft OLE DB Remoting Provider を使用して、RDS の既定の動作を暗黙的に呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="0b506-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="0b506-171">クエリは**recordset**を返すことができ、編集された**recordset**はデータソースを更新できます。</span><span class="sxs-lookup"><span data-stu-id="0b506-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="0b506-172">このチュートリアルでは ADO オブジェクトを使用して RDS を呼び出しませんが、呼び出す場合は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0b506-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="0b506-173">パート A</span><span class="sxs-lookup"><span data-stu-id="0b506-173">Part A</span></span>

<span data-ttu-id="0b506-174">この場合、RDS のみを使用していると仮定し[ます。DataControl](datacontrol-object-rds.md)を使用して、 **Recordset**オブジェクトが RDS に関連付けられるようになりました **。DataControl**。</span><span class="sxs-lookup"><span data-stu-id="0b506-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="0b506-175">[Server](submitchanges-method-rds.md) プロパティと **Connect** プロパティが引き続き設定されていれば、 [SubmitChanges](server-property-rds.md) メソッドによって [Recordset](connect-property-rds.md) オブジェクトへの変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="0b506-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a><span data-ttu-id="0b506-176">パート B</span><span class="sxs-lookup"><span data-stu-id="0b506-176">Part B</span></span>

<span data-ttu-id="0b506-177">または、connection オブジェクトと**Recordset**オブジェクトを指定して、 [rdsserver.datafactory](datafactory-object-rdsserver.md)オブジェクトを使用してサーバーを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b506-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="0b506-178">付録 a: RDS チュートリアル (VBScript)</span><span class="sxs-lookup"><span data-stu-id="0b506-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="0b506-179">これは、Microsoft Visual Basic Scripting Edition で記述された RDS チュートリアルです。</span><span class="sxs-lookup"><span data-stu-id="0b506-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="0b506-180">このチュートリアルの目的の説明については、このトピックの概要を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b506-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="0b506-181">このチュートリアルでは、 [RDS を示します。DataControl](datacontrol-object-rds.md)および[RDS。](dataspace-object-rds.md)デザイン時には、スペースが作成されます。つまり、オブジェクトタグを使用して定義されます。</span><span class="sxs-lookup"><span data-stu-id="0b506-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="0b506-182">また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b506-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="0b506-183">たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。</span><span class="sxs-lookup"><span data-stu-id="0b506-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="0b506-184">手順 1: サーバープログラムを指定する</span><span class="sxs-lookup"><span data-stu-id="0b506-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="0b506-185">vbscript は、vbscript 要求にアクセスすることによって、実行されている IIS web サーバーの名前を検出できます **。 servervariables**メソッドは、アクティブなサーバーページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b506-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="0b506-186">ただし、このチュートリアルでは、仮想サーバー "the server" を使用します。</span><span class="sxs-lookup"><span data-stu-id="0b506-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="0b506-p120">[!メモ] **ByRef** 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを **RDS.DataSpace** オブジェクトの [CreateObject](createobject-method-rds.md) メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0b506-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="0b506-191">手順2、パート A: RDS を使用してサーバープログラムを起動します。DataControl</span><span class="sxs-lookup"><span data-stu-id="0b506-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="0b506-192">次の例は、 **RDS.DataControl** の既定の動作が指定されたクエリの実行であることを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="0b506-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="0b506-193">次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="0b506-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="0b506-194">手順 4: サーバーが Recordset を返す</span><span class="sxs-lookup"><span data-stu-id="0b506-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="0b506-195">手順 5: ビジュアルコントロールが DataControl を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="0b506-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="0b506-196">手順6パート A: 変更は、RDS を使用してサーバーに送信されます。DataControl</span><span class="sxs-lookup"><span data-stu-id="0b506-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="0b506-197">次の例は、 **RDS.DataControl** がどのようにして更新を行うかを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="0b506-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="0b506-198">手順6パート B: 変更は、rdsserver.datafactory を使用してサーバーに送信されます。 DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b506-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="0b506-199">付録 B: RDS チュートリアル (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="0b506-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="0b506-p121">ADO/WFC は、[DataControl (RDS)](datacontrol-object-rds.md) オブジェクトを実装していないという点で、RDS オブジェクト モデルに完全には準拠していません。ADO/WFC は、クライアント側のクラスの [DataSpace (RDS)](dataspace-object-rds.md) のみを実装しています。</span><span class="sxs-lookup"><span data-stu-id="0b506-p121">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="0b506-p122">**DataSpace** クラスは、 [ObjectProxy](createobject-method-rds.md) オブジェクトを返す [CreateObject](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) メソッドを実装しています。 **DataSpace** クラスは、 [InternetTimeout](internettimeout-property-rds.md) プロパティも実装しています。</span><span class="sxs-lookup"><span data-stu-id="0b506-p122">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="0b506-204">**ObjectProxy** クラスは、サーバー側の任意のビジネス オブジェクトを呼び出すことができる call メソッドを実装しています。</span><span class="sxs-lookup"><span data-stu-id="0b506-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



