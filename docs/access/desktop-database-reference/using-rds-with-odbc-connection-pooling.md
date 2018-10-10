---
title: RDS を ODBC 接続プールと共に使用する
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476558"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="3ed50-102">RDS を ODBC 接続プールと共に使用する</span><span class="sxs-lookup"><span data-stu-id="3ed50-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="3ed50-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ed50-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ed50-p101">ODBC データ ソースを使用している場合は、インターネット インフォメーション サービス (IIS) の接続プール オプションを使って、クライアントの読み込みのパフォーマンスを向上できます。接続プールは接続のためのリソース マネージャーで、頻繁に使用される接続を開いた状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="3ed50-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="3ed50-106">接続プールを有効にする方法については、インターネット インフォメーション サービスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ed50-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="3ed50-107">Microsoft インターネット インフォメーション サービスのドキュメントに記載されているように、接続プールを有効にすると、Web サーバーに他の制約が適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ed50-107">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="3ed50-108">接続プールの安定性とパフォーマンスの向上を確保するには、TCP/IP ソケット ネットワーク ライブラリを使用するように Microsoft SQL Server を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ed50-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="3ed50-109">そのためには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="3ed50-109">To do this, you need to:</span></span>

  - <span data-ttu-id="3ed50-110">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する。</span><span class="sxs-lookup"><span data-stu-id="3ed50-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="3ed50-111">TCP/IP ソケットを使用するように Web サーバーを構成する。</span><span class="sxs-lookup"><span data-stu-id="3ed50-111">Configure the Web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="3ed50-112">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="3ed50-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="3ed50-113">SQL Server コンピューター上で SQL Server セットアップ プログラムを実行し、データ ソースとの対話に TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="3ed50-114">**SQL Server コンピューターで TCP/IP ソケット ネットワーク ライブラリを指定するには**</span><span class="sxs-lookup"><span data-stu-id="3ed50-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="3ed50-115">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="3ed50-116">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、 **SQL セットアップ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="3ed50-117">2 回 [**続行**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="3ed50-118">**Microsoft SQL Server-オプション**] ダイアログ ボックスでは、**ネットワーク サポートの変更**を選択し、し、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="3ed50-119">[ **TCP/IP ソケット**] チェック ボックスを選択すると、かどうかを確認し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="3ed50-120">終了するには **[続行**] をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="3ed50-121">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="3ed50-122">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**サーバー ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="3ed50-123">ダイアログ ボックスの [**全般**] タブで [**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="3ed50-124">**ネットワーク ライブラリ設定の追加**] ダイアログ ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="3ed50-125">**ポート番号**と**プロキシのアドレス**ボックスに、ネットワーク管理者から提供されたポート番号とプロキシ アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="3ed50-126">終了するには **[ok]** をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="3ed50-127">TCP/IP ソケットを使用するように Web サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="3ed50-127">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="3ed50-p102">TCP/IP ソケットを使用するように Web サーバーを構成するには、2 つの方法があります。どちらの方法を使用するかは、Web サーバーからすべての SQL Server にアクセスできるようにするか、または Web サーバーから特定の SQL Server だけにアクセスできるようにするかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="3ed50-p102">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="3ed50-p103">Web サーバーからすべての SQL Server にアクセスできるようにする場合は、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。次の手順で、この IIS Web サーバーから行われるすべての SQL Server 接続の既定のネットワーク ライブラリを変更し、TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-p103">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="3ed50-132">**Web サーバーを構成するには (すべての SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="3ed50-132">**To configure the Web server (all SQL Servers)**</span></span>

<span data-ttu-id="3ed50-133">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="3ed50-134">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="3ed50-135">**ネットワーク ライブラリ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="3ed50-136">**デフォルト ネットワーク**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="3ed50-137">変更を保存し、ユーティリティを終了する**終了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="3ed50-138">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="3ed50-139">**[スタート**] メニューからは、**プログラム**、 **Microsoft SQL Server 7.0**をポイントし、**クライアント ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="3ed50-140">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="3ed50-141">**既定のネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="3ed50-142">変更を保存し、ユーティリティを終了して **[ok]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="3ed50-p104">Web サーバーから特定の SQL Server だけにアクセスできるようにする場合は、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。特定の SQL Server 接続のネットワーク ライブラリを変更するには、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-p104">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<span data-ttu-id="3ed50-145">**Web サーバーを構成するには (特定の SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="3ed50-145">**To configure the Web server (a specific SQL Server)**</span></span>

<span data-ttu-id="3ed50-146">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="3ed50-147">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="3ed50-148">[**詳細設定**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="3ed50-149">[**サーバー** ] ボックスで、 **TCP/IP ソケット**を使用する接続先のサーバーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="3ed50-150">[ **DLL 名**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="3ed50-151">**追加/変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-151">Click **Add/Modify**.</span></span> <span data-ttu-id="3ed50-152">このサーバーをポイントするすべてのデータ ソースが TCP/IP ソケットを使用ようになりました。</span><span class="sxs-lookup"><span data-stu-id="3ed50-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="3ed50-153">**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-153">Click **Done**.</span></span>

<span data-ttu-id="3ed50-154">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="3ed50-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="3ed50-155">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="3ed50-156">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="3ed50-157">**[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-157">Click **Add**.</span></span>

4.  <span data-ttu-id="3ed50-158">**サーバー別名**] ボックスで、サーバーの別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="3ed50-159">[**ネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="3ed50-160">[**コンピューター名**] ボックスで、TCP/IP ソケット クライアントをリッスンしているコンピューターのコンピューター名を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="3ed50-161">[**ポート番号**] ボックスで、SQL Server がリッスンするポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ed50-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="3ed50-162">**[Ok]**、し **[ok]** もう一度ユーティリティを終了する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ed50-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

