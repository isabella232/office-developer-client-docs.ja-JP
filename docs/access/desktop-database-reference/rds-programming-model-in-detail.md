---
title: RDS プログラミング モデルの詳細
TOCTitle: RDS Programming Model in Detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 123a50a48407f82d11e704ce611896875d0017e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476867"
---
# <a name="rds-programming-model-in-detail"></a><span data-ttu-id="2aa85-102">RDS プログラミング モデルの詳細</span><span class="sxs-lookup"><span data-stu-id="2aa85-102">RDS Programming Model in Detail</span></span>


<span data-ttu-id="2aa85-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2aa85-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="2aa85-104">RDS プログラミング モデルの主な要素は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2aa85-104">The following are key elements of the RDS programming model:</span></span>

  - <span data-ttu-id="2aa85-105">RDS.インスタンス</span><span class="sxs-lookup"><span data-stu-id="2aa85-105">RDS.DataSpace</span></span>

  - <span data-ttu-id="2aa85-106">RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2aa85-106">RDSServer.DataFactory</span></span>

  - <span data-ttu-id="2aa85-107">RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="2aa85-107">RDS.DataControl</span></span>

  - <span data-ttu-id="2aa85-108">イベント</span><span class="sxs-lookup"><span data-stu-id="2aa85-108">Event</span></span>

## <a name="rdsdataspace"></a><span data-ttu-id="2aa85-109">RDS.インスタンス</span><span class="sxs-lookup"><span data-stu-id="2aa85-109">RDS.DataSpace</span></span>

<span data-ttu-id="2aa85-p101">クライアント アプリケーションでは、サーバーおよび呼び出すサーバー プログラムを指定する必要があります。それに対し、クライアント アプリケーションはサーバー プログラムへの参照を受け取り、その参照をサーバー プログラムそのものと同じように扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p101">Your client application must specify the server and the server program to invoke. In return, your application receives a reference to the server program and can treat the reference as if it were the server program itself.</span></span>

<span data-ttu-id="2aa85-112">RDS オブジェクト モデルでは、この機能は [RDS.DataSpace](dataspace-object-rds.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="2aa85-112">The RDS object model embodies this functionality with the [RDS.DataSpace](dataspace-object-rds.md) object.</span></span>

<span data-ttu-id="2aa85-p102">サーバー プログラムは、プログラム識別子 (*ProgID*) で指定します。サーバーは、*ProgID* とサーバー コンピューターのレジストリを使用して、実際に起動するプログラムに関する情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p102">The server program is specified with a program identifier, or *ProgID*. The server uses the *ProgID* and the server machine's registry to locate information about the actual program to initiate.</span></span>

<span data-ttu-id="2aa85-p103">RDS は、サーバー プログラムを、インターネットまたはイントラネット上のリモート サーバー、ローカル エリア ネットワーク上のサーバー、またはサーバーではなくローカルのダイナミック リンク ライブラリ (DLL) のどこに存在するかによって、内部的に区別します。この区別に基づいて、クライアントとサーバーとの間で情報を交換する方法を決定し、クライアント アプリケーションに返される参照の種類を明確に区別します。ただし、ユーザーにとっては、この区別は特別な意味を持ちません。ユーザーにとって重要なのは、使用可能なプログラム参照を受け取るということだけです。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p103">RDS makes a distinction internally depending on whether the server program is on a remote server across the Internet or an intranet; a server on a local area network; or not on a server at all, but instead on a local dynamic-link library (DLL). This distinction determines how information is exchanged between the client and the server, and makes a tangible difference in the type of reference returned to your client application. However, from your point of view, this distinction has no special meaning. All that matters is that you receive a usable program reference.</span></span>

## <a name="rdsserverdatafactory"></a><span data-ttu-id="2aa85-119">RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2aa85-119">RDSServer.DataFactory</span></span>

<span data-ttu-id="2aa85-120">RDS が提供する既定のサーバー プログラムは、データ ソースに対して SQL クエリを実行して [Recordset](recordset-object-ado.md) オブジェクトを返すか、または **Recordset** オブジェクトを受け取ってデータ ソースを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-120">RDS provides a default server program that can either perform a SQL query against the data source and return a [Recordset](recordset-object-ado.md) object or take a **Recordset** object and update the data source.</span></span>

<span data-ttu-id="2aa85-121">RDS オブジェクト モデルでは、この機能は [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="2aa85-121">The RDS object model embodies this functionality with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

<span data-ttu-id="2aa85-122">さらに、このオブジェクトには、プログラムによりデータを格納できる空の **Recordset** オブジェクトを作成するためのメソッド ([CreateRecordset](createrecordset-method-rds.md))、および **Recordset** オブジェクトを Web ページ作成用のテキスト文字列に変換するためのメソッド ([ConvertToString](converttostring-method-rds.md)) があります。</span><span class="sxs-lookup"><span data-stu-id="2aa85-122">In addition, this object has a method for creating an empty **Recordset** object that you can fill programmatically ([CreateRecordset](createrecordset-method-rds.md)), and another method for converting a **Recordset** object into a text string to build a Web page ([ConvertToString](converttostring-method-rds.md)).</span></span>

<span data-ttu-id="2aa85-123">ADO では、 **DataFactory** ハンドラーの **RDSServer.DataFactory** の既定の接続およびコマンドの動作の一部、および接続、コマンド、セキュリティなどのパラメーターが格納されたカスタマイズ ファイルを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-123">With ADO, you can override some of the standard connection and command behavior of the **RDSServer.DataFactory** with a **DataFactory** handler and a customization file that contains connection, command, and security parameters.</span></span>

<span data-ttu-id="2aa85-124">サーバー プログラムは、*ビジネス オブジェクト*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-124">The server program is sometimes called a *business object*.</span></span> <span data-ttu-id="2aa85-125">複雑なデータ アクセスや妥当性検査を実行できる、独自のカスタム ビジネス オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-125">You can write your own custom business object that can perform complicated data access, validity checks, and so on.</span></span> <span data-ttu-id="2aa85-126">カスタム ビジネス オブジェクトを作成する場合は、 **RDSServer.DataFactory**オブジェクトのインスタンスを作成およびそのメソッドの一部を使用して、独自のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="2aa85-126">Even when writing a custom business object, you can create an instance of an **RDSServer.DataFactory** object and use some of its methods to accomplish your own tasks.</span></span>

## <a name="rdsdatacontrol"></a><span data-ttu-id="2aa85-127">RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="2aa85-127">RDS.DataControl</span></span>

<span data-ttu-id="2aa85-p105">RDS では、 **RDS.DataSpace** と **RDSServer.DataFactory** の機能を組み合わせるための手段、およびクエリの結果としてデータ ソースから返される **Recordset** オブジェクトを、ビジュアル コントロールで容易に使用できるようにするための手段が提供されています。通常、RDS は、可能な限り自動的に、サーバー上の情報にアクセスしてビジュアル コントロールにその情報を表示しようとします。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p105">RDS provides a means to combine the functionality of the **RDS.DataSpace** and **RDSServer.DataFactory**, and also enable visual controls to easily use the **Recordset** object returned by a query from a data source. RDS attempts, for the most common case, to do as much as possible to automatically gain access to information on a server and display it in a visual control.</span></span>

<span data-ttu-id="2aa85-130">RDS オブジェクト モデルでは、この機能は [RDS.DataControl](datacontrol-object-rds.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="2aa85-130">The RDS object model embodies this functionality with the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

<span data-ttu-id="2aa85-p106">**RDS.DataControl** には 2 つの側面があります。1 つはデータ ソースに関する側面です。 **RDS.DataControl** の **Connect** プロパティおよび **SQL** プロパティを使用して、コマンドおよび接続の情報を設定すると、自動的に **RDS.DataSpace** が使用されて、既定の **RDSServer.DataFactory** オブジェクトへの参照が作成されます。その後、 **RDSServer.DataFactory** は、 **Connect** プロパティの値を使用してデータ ソースに接続し、 **SQL** プロパティの値を使用してデータ ソースから **Recordset** を取得して、 **Recordset** オブジェクトを **RDS.DataControl** に返します。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p106">The **RDS.DataControl** has two aspects. One aspect pertains to the data source. If you set the command and connection information using the **Connect** and **SQL** properties of the **RDS.DataControl**, it will automatically use the **RDS.DataSpace** to create a reference to the default **RDSServer.DataFactory** object. Then the **RDSServer.DataFactory** will use the **Connect** property value to connect to the data source, use the **SQL** property value to obtain a **Recordset** from the data source, and return the **Recordset** object to the **RDS.DataControl**.</span></span>

<span data-ttu-id="2aa85-p107">もう 1 つの側面は、返された **Recordset** 情報のビジュアル コントロールでの表示に関するものです。ビジュアル コントロールをバインディングという処理によって **RDS.DataControl** に関連付け、関連する **Recordset** オブジェクトに含まれる情報にアクセスし、クエリの結果を Microsoft® Internet Explorer で Web ページに表示することができます。各 **RDS.DataControl** オブジェクトは、単一のクエリの結果を表す 1 つの **Recordset** オブジェクトを、1 つまたは複数のビジュアル コントロール (テキスト ボックス、コンボ ボックス、グリッド コントロールなど) にバインドします。各ページに複数の **RDS.DataControl** オブジェクトが存在する場合があります。それぞれの **RDS.DataControl** オブジェクトを異なるデータ ソースに接続し、別のクエリの結果を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p107">The second aspect pertains to the display of returned **Recordset** information in a visual control. You can associate a visual control with the **RDS.DataControl** (in a process called binding) and gain access to the information in the associated **Recordset** object, displaying query results on a Web page in Microsoft® Internet Explorer. Each **RDS.DataControl** object binds one **Recordset** object, representing the results of a single query, to one or more visual controls (for example, a text box, combo box, grid control, and so forth). There may be more than one **RDS.DataControl** object on each page. Each **RDS.DataControl** object can be connected to a different data source and contain the results of a separate query.</span></span>

<span data-ttu-id="2aa85-p108">また、 **RDS.DataControl** オブジェクトには、関連する **Recordset** オブジェクトの行に対して移動、並べ替え、およびフィルター選択を行うためのメソッドがあります。これらのメソッドは、ADO の **Recordset** オブジェクトのメソッドと似ていますが、同じではありません。</span><span class="sxs-lookup"><span data-stu-id="2aa85-p108">The **RDS.DataControl** object also has its own methods for navigating, sorting, and filtering the rows of the associated **Recordset** object. These methods are similar, but not the same as the methods on the ADO **Recordset** object.</span></span>

## <a name="events"></a><span data-ttu-id="2aa85-142">イベント</span><span class="sxs-lookup"><span data-stu-id="2aa85-142">Events</span></span>

<span data-ttu-id="2aa85-143">RDS は、2 種類の独自のイベントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2aa85-143">RDS supports two of its own events, which are independent of the ADO event model.</span></span> <span data-ttu-id="2aa85-144">[OnReadyStateChange](onreadystatechange-event-rds.md)イベントが呼び出されたときに**の rds.DataControl** [ReadyState](readystate-property-rds.md)プロパティの変更、非同期操作が正常に完了を通知する、終了、またはエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="2aa85-144">The [onReadyStateChange](onreadystatechange-event-rds.md) event is called whenever the **RDS.DataControl** [ReadyState](readystate-property-rds.md) property changes, thus notifying you when an asynchronous operation has successfully completed, terminated, or experienced an error.</span></span> <span data-ttu-id="2aa85-145">[onError](onerror-event-rds.md) イベントはエラーが発生するたびに (エラーが非同期操作の途中で発生した場合でも) 呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2aa85-145">The [onError](onerror-event-rds.md) event is called whenever an error occurs, even if the error occurs during an asynchronous operation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2aa85-146">[!メモ] Microsoft Internet Explorer は、 <STRONG>onDataSetChanged</STRONG> ( <STRONG>Recordset</STRONG> は有効だが、まだ行を取得している) および <STRONG>onDataSetComplete</STRONG> ( <STRONG>Recordset</STRONG> は行の取得を終了した) という 2 つの追加イベントを提供します。</span><span class="sxs-lookup"><span data-stu-id="2aa85-146">Microsoft Internet Explorer provides two additional events to RDS — <STRONG>onDataSetChanged</STRONG> (the <STRONG>Recordset</STRONG> is functional but still retrieving rows) and <STRONG>onDataSetComplete</STRONG> (the <STRONG>Recordset</STRONG> has finished retrieving rows).</span></span></P>


