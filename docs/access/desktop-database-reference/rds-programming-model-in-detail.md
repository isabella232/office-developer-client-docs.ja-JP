---
title: RDS のプログラミング モデルの詳細
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea0f47e8ad86ecac4dd2423c289e3891cd7c6719
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998526"
---
# <a name="rds-programming-model-in-detail"></a><span data-ttu-id="69062-102">RDS のプログラミング モデルの詳細</span><span class="sxs-lookup"><span data-stu-id="69062-102">RDS programming model in detail</span></span>

<span data-ttu-id="69062-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="69062-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69062-104">RDS プログラミング モデルの主な要素は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="69062-104">The following are key elements of the RDS programming model:</span></span>

- <span data-ttu-id="69062-105">RDS.インスタンス</span><span class="sxs-lookup"><span data-stu-id="69062-105">RDS.DataSpace</span></span>
- <span data-ttu-id="69062-106">RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="69062-106">RDSServer.DataFactory</span></span>
- <span data-ttu-id="69062-107">RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="69062-107">RDS.DataControl</span></span>
- <span data-ttu-id="69062-108">イベント</span><span class="sxs-lookup"><span data-stu-id="69062-108">Event</span></span>

## <a name="rdsdataspace"></a><span data-ttu-id="69062-109">RDS.インスタンス</span><span class="sxs-lookup"><span data-stu-id="69062-109">RDS.DataSpace</span></span>

<span data-ttu-id="69062-p101">クライアント アプリケーションでは、サーバーおよび呼び出すサーバー プログラムを指定する必要があります。それに対し、クライアント アプリケーションはサーバー プログラムへの参照を受け取り、その参照をサーバー プログラムそのものと同じように扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="69062-p101">Your client application must specify the server and the server program to invoke. In return, your application receives a reference to the server program and can treat the reference as if it were the server program itself.</span></span>

<span data-ttu-id="69062-112">RDS オブジェクト モデルでは、この機能は [RDS.DataSpace](dataspace-object-rds.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="69062-112">The RDS object model embodies this functionality with the [RDS.DataSpace](dataspace-object-rds.md) object.</span></span>

<span data-ttu-id="69062-p102">サーバー プログラムは、プログラム識別子 (*ProgID*) で指定します。サーバーは、*ProgID* とサーバー コンピューターのレジストリを使用して、実際に起動するプログラムに関する情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="69062-p102">The server program is specified with a program identifier, or *ProgID*. The server uses the *ProgID* and the server machine's registry to locate information about the actual program to initiate.</span></span>

<span data-ttu-id="69062-p103">RDS は、サーバー プログラムを、インターネットまたはイントラネット上のリモート サーバー、ローカル エリア ネットワーク上のサーバー、またはサーバーではなくローカルのダイナミック リンク ライブラリ (DLL) のどこに存在するかによって、内部的に区別します。この区別に基づいて、クライアントとサーバーとの間で情報を交換する方法を決定し、クライアント アプリケーションに返される参照の種類を明確に区別します。ただし、ユーザーにとっては、この区別は特別な意味を持ちません。ユーザーにとって重要なのは、使用可能なプログラム参照を受け取るということだけです。</span><span class="sxs-lookup"><span data-stu-id="69062-p103">RDS makes a distinction internally depending on whether the server program is on a remote server across the Internet or an intranet; a server on a local area network; or not on a server at all, but instead on a local dynamic-link library (DLL). This distinction determines how information is exchanged between the client and the server, and makes a tangible difference in the type of reference returned to your client application. However, from your point of view, this distinction has no special meaning. All that matters is that you receive a usable program reference.</span></span>

## <a name="rdsserverdatafactory"></a><span data-ttu-id="69062-119">RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="69062-119">RDSServer.DataFactory</span></span>

<span data-ttu-id="69062-120">RDS が提供する既定のサーバー プログラムは、データ ソースに対して SQL クエリを実行して [Recordset](recordset-object-ado.md) オブジェクトを返すか、または **Recordset** オブジェクトを受け取ってデータ ソースを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="69062-120">RDS provides a default server program that can either perform a SQL query against the data source and return a [Recordset](recordset-object-ado.md) object or take a **Recordset** object and update the data source.</span></span>

<span data-ttu-id="69062-121">RDS オブジェクト モデルでは、この機能は [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="69062-121">The RDS object model embodies this functionality with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

<span data-ttu-id="69062-122">さらにこのオブジェクトは、プログラムを使用して入力できる空の**レコード セット**オブジェクトを作成するためのメソッド ([CreateRecordset](createrecordset-method-rds.md)) と ([の web ページを作成するテキスト文字列、**レコード セット**オブジェクトに変換するための別の方法ConvertToString](converttostring-method-rds.md))。</span><span class="sxs-lookup"><span data-stu-id="69062-122">In addition, this object has a method for creating an empty **Recordset** object that you can fill programmatically ([CreateRecordset](createrecordset-method-rds.md)), and another method for converting a **Recordset** object into a text string to build a webpage ([ConvertToString](converttostring-method-rds.md)).</span></span>

<span data-ttu-id="69062-123">ADO では、 **DataFactory** ハンドラーの **RDSServer.DataFactory** の既定の接続およびコマンドの動作の一部、および接続、コマンド、セキュリティなどのパラメーターが格納されたカスタマイズ ファイルを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="69062-123">With ADO, you can override some of the standard connection and command behavior of the **RDSServer.DataFactory** with a **DataFactory** handler and a customization file that contains connection, command, and security parameters.</span></span>

<span data-ttu-id="69062-124">サーバー プログラムは、*ビジネス オブジェクト*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="69062-124">The server program is sometimes called a *business object*.</span></span> <span data-ttu-id="69062-125">複雑なデータ アクセスや妥当性検査を実行できる、独自のカスタム ビジネス オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="69062-125">You can write your own custom business object that can perform complicated data access, validity checks, and so on.</span></span> <span data-ttu-id="69062-126">カスタム ビジネス オブジェクトを作成する場合は、 **RDSServer.DataFactory**オブジェクトのインスタンスを作成およびそのメソッドの一部を使用して、独自のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="69062-126">Even when writing a custom business object, you can create an instance of an **RDSServer.DataFactory** object and use some of its methods to accomplish your own tasks.</span></span>

## <a name="rdsdatacontrol"></a><span data-ttu-id="69062-127">RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="69062-127">RDS.DataControl</span></span>

<span data-ttu-id="69062-p105">RDS では、 **RDS.DataSpace** と **RDSServer.DataFactory** の機能を組み合わせるための手段、およびクエリの結果としてデータ ソースから返される **Recordset** オブジェクトを、ビジュアル コントロールで容易に使用できるようにするための手段が提供されています。通常、RDS は、可能な限り自動的に、サーバー上の情報にアクセスしてビジュアル コントロールにその情報を表示しようとします。</span><span class="sxs-lookup"><span data-stu-id="69062-p105">RDS provides a means to combine the functionality of the **RDS.DataSpace** and **RDSServer.DataFactory**, and also enable visual controls to easily use the **Recordset** object returned by a query from a data source. RDS attempts, for the most common case, to do as much as possible to automatically gain access to information on a server and display it in a visual control.</span></span>

<span data-ttu-id="69062-130">RDS オブジェクト モデルでは、この機能は [RDS.DataControl](datacontrol-object-rds.md) オブジェクトに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="69062-130">The RDS object model embodies this functionality with the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

<span data-ttu-id="69062-p106">**RDS.DataControl** には 2 つの側面があります。1 つはデータ ソースに関する側面です。 **RDS.DataControl** の **Connect** プロパティおよび **SQL** プロパティを使用して、コマンドおよび接続の情報を設定すると、自動的に **RDS.DataSpace** が使用されて、既定の **RDSServer.DataFactory** オブジェクトへの参照が作成されます。その後、 **RDSServer.DataFactory** は、 **Connect** プロパティの値を使用してデータ ソースに接続し、 **SQL** プロパティの値を使用してデータ ソースから **Recordset** を取得して、 **Recordset** オブジェクトを **RDS.DataControl** に返します。</span><span class="sxs-lookup"><span data-stu-id="69062-p106">The **RDS.DataControl** has two aspects. One aspect pertains to the data source. If you set the command and connection information using the **Connect** and **SQL** properties of the **RDS.DataControl**, it will automatically use the **RDS.DataSpace** to create a reference to the default **RDSServer.DataFactory** object. Then the **RDSServer.DataFactory** will use the **Connect** property value to connect to the data source, use the **SQL** property value to obtain a **Recordset** from the data source, and return the **Recordset** object to the **RDS.DataControl**.</span></span>

<span data-ttu-id="69062-135">もう 1 つの側面は、返された **Recordset** 情報のビジュアル コントロールでの表示に関するものです。</span><span class="sxs-lookup"><span data-stu-id="69062-135">The second aspect pertains to the display of returned **Recordset** information in a visual control.</span></span> <span data-ttu-id="69062-136">**Rds. のビジュアル コントロールを関連付けることができます。DataControl** (バインドと呼ばれるプロセス) で、Microsoft Internet Explorer で web ページのクエリ結果を表示する、関連付けられた**レコード セット**オブジェクト内の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="69062-136">You can associate a visual control with the **RDS.DataControl** (in a process called binding) and gain access to the information in the associated **Recordset** object, displaying query results on a webpage in Microsoft Internet Explorer.</span></span> <span data-ttu-id="69062-137">各 **RDS.DataControl** オブジェクトは、単一のクエリの結果を表す 1 つの **Recordset** オブジェクトを、1 つまたは複数のビジュアル コントロール (テキスト ボックス、コンボ ボックス、グリッド コントロールなど) にバインドします。</span><span class="sxs-lookup"><span data-stu-id="69062-137">Each **RDS.DataControl** object binds one **Recordset** object, representing the results of a single query, to one or more visual controls (for example, a text box, combo box, grid control, and so forth).</span></span> <span data-ttu-id="69062-138">各ページに複数の **RDS.DataControl** オブジェクトが存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="69062-138">There may be more than one **RDS.DataControl** object on each page.</span></span> <span data-ttu-id="69062-139">それぞれの **RDS.DataControl** オブジェクトを異なるデータ ソースに接続し、別のクエリの結果を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="69062-139">Each **RDS.DataControl** object can be connected to a different data source and contain the results of a separate query.</span></span>

<span data-ttu-id="69062-p108">また、 **RDS.DataControl** オブジェクトには、関連する **Recordset** オブジェクトの行に対して移動、並べ替え、およびフィルター選択を行うためのメソッドがあります。これらのメソッドは、ADO の **Recordset** オブジェクトのメソッドと似ていますが、同じではありません。</span><span class="sxs-lookup"><span data-stu-id="69062-p108">The **RDS.DataControl** object also has its own methods for navigating, sorting, and filtering the rows of the associated **Recordset** object. These methods are similar, but not the same as the methods on the ADO **Recordset** object.</span></span>

## <a name="events"></a><span data-ttu-id="69062-142">イベント</span><span class="sxs-lookup"><span data-stu-id="69062-142">Events</span></span>

<span data-ttu-id="69062-143">RDS は、2 種類の独自のイベントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="69062-143">RDS supports two of its own events, which are independent of the ADO event model.</span></span> <span data-ttu-id="69062-144">[OnReadyStateChange](onreadystatechange-event-rds.md)イベントが呼び出されたときに**の rds.DataControl** [ReadyState](readystate-property-rds.md)プロパティの変更、非同期操作が正常に完了を通知する、終了、またはエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="69062-144">The [onReadyStateChange](onreadystatechange-event-rds.md) event is called whenever the **RDS.DataControl** [ReadyState](readystate-property-rds.md) property changes, thus notifying you when an asynchronous operation has successfully completed, terminated, or experienced an error.</span></span> <span data-ttu-id="69062-145">[onError](onerror-event-rds.md) イベントはエラーが発生するたびに (エラーが非同期操作の途中で発生した場合でも) 呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="69062-145">The [onError](onerror-event-rds.md) event is called whenever an error occurs, even if the error occurs during an asynchronous operation.</span></span>

> [!NOTE]
> <span data-ttu-id="69062-146">[!メモ] Microsoft Internet Explorer は、 **onDataSetChanged** ( **Recordset** は有効だが、まだ行を取得している) および **onDataSetComplete** ( **Recordset** は行の取得を終了した) という 2 つの追加イベントを提供します。</span><span class="sxs-lookup"><span data-stu-id="69062-146">Microsoft Internet Explorer provides two additional events to RDS — **onDataSetChanged** (the **Recordset** is functional but still retrieving rows) and **onDataSetComplete** (the **Recordset** has finished retrieving rows).</span></span>


