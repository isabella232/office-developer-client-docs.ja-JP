---
title: RDS を ODBC 接続プールと共に使用する
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706367"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="75cdf-102">RDS を ODBC 接続プールと共に使用する</span><span class="sxs-lookup"><span data-stu-id="75cdf-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="75cdf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="75cdf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75cdf-p101">ODBC データ ソースを使用している場合は、インターネット インフォメーション サービス (IIS) の接続プール オプションを使って、クライアントの読み込みのパフォーマンスを向上できます。接続プールは接続のためのリソース マネージャーで、頻繁に使用される接続を開いた状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="75cdf-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="75cdf-106">接続プールを有効にする方法については、インターネット インフォメーション サービスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75cdf-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="75cdf-107">接続プールを有効にすることがあります件名の web サーバーに他の制約では、Microsoft インターネット インフォメーション サービスのドキュメントで説明したように注意してください。</span><span class="sxs-lookup"><span data-stu-id="75cdf-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="75cdf-108">接続プールの安定性とパフォーマンスの向上を確保するには、TCP/IP ソケット ネットワーク ライブラリを使用するように Microsoft SQL Server を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75cdf-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="75cdf-109">そのためには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="75cdf-109">To do this, you need to:</span></span>

  - <span data-ttu-id="75cdf-110">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する。</span><span class="sxs-lookup"><span data-stu-id="75cdf-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="75cdf-111">TCP/IP ソケットを使用する web サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="75cdf-112">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="75cdf-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="75cdf-113">SQL Server コンピューター上で SQL Server セットアップ プログラムを実行し、データ ソースとの対話に TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="75cdf-114">**SQL Server コンピューターで TCP/IP ソケット ネットワーク ライブラリを指定するには**</span><span class="sxs-lookup"><span data-stu-id="75cdf-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="75cdf-115">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="75cdf-116">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、 **SQL セットアップ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="75cdf-117">2 回 [**続行**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="75cdf-118">**Microsoft SQL Server-オプション**] ダイアログ ボックスでは、**ネットワーク サポートの変更**を選択し、し、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="75cdf-119">[ **TCP/IP ソケット**] チェック ボックスを選択すると、かどうかを確認し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="75cdf-120">終了するには **[続行**] をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="75cdf-121">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="75cdf-122">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**サーバー ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="75cdf-123">ダイアログ ボックスの [**全般**] タブで [**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="75cdf-124">**ネットワーク ライブラリ設定の追加**] ダイアログ ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="75cdf-125">**ポート番号**と**プロキシのアドレス**ボックスに、ネットワーク管理者から提供されたポート番号とプロキシ アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="75cdf-126">終了するには **[ok]** をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="75cdf-127">Web サーバーが TCP/IP ソケットを使用するを構成します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="75cdf-128">TCP/IP ソケットを使用する web サーバーを構成する 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="75cdf-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="75cdf-129">Web サーバーからすべての SQL サーバーをアクセスするかどうかに依存するは、または web サーバーから特定の SQL Server だけにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="75cdf-130">すべての SQL サーバーには web サーバーからアクセスした場合は、web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75cdf-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="75cdf-131">次の手順では、TCP/IP ソケット ネットワーク ライブラリを使用するのには、この IIS web サーバーから作成されたすべての SQL Server 接続の既定のネットワーク ライブラリを変更します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="75cdf-132">**Web サーバー (すべての SQL サーバー) を構成するには**</span><span class="sxs-lookup"><span data-stu-id="75cdf-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="75cdf-133">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="75cdf-134">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="75cdf-135">**ネットワーク ライブラリ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="75cdf-136">**デフォルト ネットワーク**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="75cdf-137">変更を保存し、ユーティリティを終了する**終了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="75cdf-138">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="75cdf-139">**[スタート**] メニューからは、**プログラム**、 **Microsoft SQL Server 7.0**をポイントし、**クライアント ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="75cdf-140">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="75cdf-141">**既定のネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="75cdf-142">変更を保存し、ユーティリティを終了して **[ok]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="75cdf-143">Web サーバーから特定の SQL Server にアクセスした場合は、web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75cdf-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="75cdf-144">特定の SQL Server 接続のネットワーク ライブラリを変更するには、次のように web サーバー コンピューターで SQL Server クライアント ソフトウェアを構成します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="75cdf-145">**(特定の SQL Server) の web サーバーを構成するのには**</span><span class="sxs-lookup"><span data-stu-id="75cdf-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="75cdf-146">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="75cdf-147">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="75cdf-148">[**詳細設定**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="75cdf-149">[**サーバー** ] ボックスで、 **TCP/IP ソケット**を使用する接続先のサーバーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="75cdf-150">[ **DLL 名**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="75cdf-151">**追加/変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-151">Click **Add/Modify**.</span></span> <span data-ttu-id="75cdf-152">このサーバーをポイントするすべてのデータ ソースが TCP/IP ソケットを使用ようになりました。</span><span class="sxs-lookup"><span data-stu-id="75cdf-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="75cdf-153">**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-153">Click **Done**.</span></span>

<span data-ttu-id="75cdf-154">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="75cdf-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="75cdf-155">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="75cdf-156">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="75cdf-157">**[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-157">Click **Add**.</span></span>

4.  <span data-ttu-id="75cdf-158">**サーバー別名**] ボックスで、サーバーの別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="75cdf-159">[**ネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="75cdf-160">[**コンピューター名**] ボックスで、TCP/IP ソケット クライアントをリッスンしているコンピューターのコンピューター名を入力します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="75cdf-161">[**ポート番号**] ボックスで、SQL Server がリッスンするポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="75cdf-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="75cdf-162">**[Ok]**、し **[ok]** もう一度ユーティリティを終了する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75cdf-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

