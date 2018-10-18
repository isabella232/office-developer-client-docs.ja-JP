---
title: RDS を ODBC 接続プールと共に使用する
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee66e68cb8eeaaca57c007dc64a9e2b3a8476ec7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606018"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="bc5c6-102">RDS を ODBC 接続プールと共に使用する</span><span class="sxs-lookup"><span data-stu-id="bc5c6-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="bc5c6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc5c6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bc5c6-p101">ODBC データ ソースを使用している場合は、インターネット インフォメーション サービス (IIS) の接続プール オプションを使って、クライアントの読み込みのパフォーマンスを向上できます。接続プールは接続のためのリソース マネージャーで、頻繁に使用される接続を開いた状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="bc5c6-106">接続プールを有効にする方法については、インターネット インフォメーション サービスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="bc5c6-107"><<<<<<<、接続プーリングを有効にすることがあります件名の Web サーバーに他の制約では、Microsoft インターネット インフォメーション サービスのドキュメントで説明したように注意してください。 ヘッドです。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-107"><<<<<<< HEAD Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
<span data-ttu-id="bc5c6-108">=== 接続プールを有効にすることがあります件名の web サーバーに他の制約では、Microsoft インターネット インフォメーション サービスのドキュメントで説明したように注意してくださいしてください。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-108">======= Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
>>>>>>> <span data-ttu-id="bc5c6-109">master</span><span class="sxs-lookup"><span data-stu-id="bc5c6-109">master</span></span>

<span data-ttu-id="bc5c6-110">接続プールの安定性とパフォーマンスの向上を確保するには、TCP/IP ソケット ネットワーク ライブラリを使用するように Microsoft SQL Server を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-110">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="bc5c6-111">そのためには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-111">To do this, you need to:</span></span>

  - <span data-ttu-id="bc5c6-112">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-112">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

<span data-ttu-id="bc5c6-113"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="bc5c6-113"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="bc5c6-114">TCP/IP ソケットを使用するように Web サーバーを構成する。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-114">Configure the Web server to use TCP/IP Sockets.</span></span>
=======
  - <span data-ttu-id="bc5c6-115">TCP/IP ソケットを使用する web サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-115">Configure the web server to use TCP/IP Sockets.</span></span>
>>>>>>> <span data-ttu-id="bc5c6-116">master</span><span class="sxs-lookup"><span data-stu-id="bc5c6-116">master</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="bc5c6-117">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="bc5c6-117">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="bc5c6-118">SQL Server コンピューター上で SQL Server セットアップ プログラムを実行し、データ ソースとの対話に TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-118">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="bc5c6-119">**SQL Server コンピューターで TCP/IP ソケット ネットワーク ライブラリを指定するには**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-119">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="bc5c6-120">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-120">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="bc5c6-121">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、 **SQL セットアップ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-121">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="bc5c6-122">2 回 [**続行**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-122">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="bc5c6-123">**Microsoft SQL Server-オプション**] ダイアログ ボックスでは、**ネットワーク サポートの変更**を選択し、し、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-123">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="bc5c6-124">[ **TCP/IP ソケット**] チェック ボックスを選択すると、かどうかを確認し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-124">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="bc5c6-125">終了するには **[続行**] をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-125">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="bc5c6-126">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-126">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="bc5c6-127">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**サーバー ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-127">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="bc5c6-128">ダイアログ ボックスの [**全般**] タブで [**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-128">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="bc5c6-129">**ネットワーク ライブラリ設定の追加**] ダイアログ ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-129">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="bc5c6-130">**ポート番号**と**プロキシのアドレス**ボックスに、ネットワーク管理者から提供されたポート番号とプロキシ アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-130">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="bc5c6-131">終了するには **[ok]** をクリックし、セットアップを終了します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-131">Click **OK** to finish, and exit setup.</span></span>

<span data-ttu-id="bc5c6-132"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="bc5c6-132"><<<<<<< HEAD</span></span>
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="bc5c6-133">TCP/IP ソケットを使用するように Web サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="bc5c6-133">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="bc5c6-p103">TCP/IP ソケットを使用するように Web サーバーを構成するには、2 つの方法があります。どちらの方法を使用するかは、Web サーバーからすべての SQL Server にアクセスできるようにするか、または Web サーバーから特定の SQL Server だけにアクセスできるようにするかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-p103">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="bc5c6-p104">Web サーバーからすべての SQL Server にアクセスできるようにする場合は、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。次の手順で、この IIS Web サーバーから行われるすべての SQL Server 接続の既定のネットワーク ライブラリを変更し、TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-p104">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<a name="to-configure-the-web-server-all-sql-servers"></a><span data-ttu-id="bc5c6-138">**Web サーバーを構成するには (すべての SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-138">**To configure the Web server (all SQL Servers)**</span></span>
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="bc5c6-139">Web サーバーが TCP/IP ソケットを使用するを構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-139">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="bc5c6-140">TCP/IP ソケットを使用する web サーバーを構成する 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-140">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="bc5c6-141">Web サーバーからすべての SQL サーバーをアクセスするかどうかに依存するは、または web サーバーから特定の SQL Server だけにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-141">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="bc5c6-142">すべての SQL サーバーには web サーバーからアクセスした場合は、web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-142">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="bc5c6-143">次の手順では、TCP/IP ソケット ネットワーク ライブラリを使用するのには、この IIS web サーバーから作成されたすべての SQL Server 接続の既定のネットワーク ライブラリを変更します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-143">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="bc5c6-144">**Web サーバー (すべての SQL サーバー) を構成するには**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-144">**To configure the web server (all SQL Servers)**</span></span>
>>>>>>> <span data-ttu-id="bc5c6-145">master</span><span class="sxs-lookup"><span data-stu-id="bc5c6-145">master</span></span>

<span data-ttu-id="bc5c6-146">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="bc5c6-147">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="bc5c6-148">**ネットワーク ライブラリ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-148">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="bc5c6-149">**デフォルト ネットワーク**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-149">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="bc5c6-150">変更を保存し、ユーティリティを終了する**終了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-150">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="bc5c6-151">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-151">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="bc5c6-152">**[スタート**] メニューからは、**プログラム**、 **Microsoft SQL Server 7.0**をポイントし、**クライアント ネットワーク ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-152">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="bc5c6-153">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-153">Click the **General** tab.</span></span>

3.  <span data-ttu-id="bc5c6-154">**既定のネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-154">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="bc5c6-155">変更を保存し、ユーティリティを終了して **[ok]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-155">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="bc5c6-156"><<<<<<< ヘッド、特定の SQL Server にアクセスすると Web サーバーから、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-156"><<<<<<< HEAD If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="bc5c6-157">特定の SQL Server 接続のネットワーク ライブラリを変更するには、Web サーバー コンピューターで SQL Server クライアント設定ユーティリティを次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-157">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<a name="to-configure-the-web-server-a-specific-sql-server"></a><span data-ttu-id="bc5c6-158">**Web サーバーを構成するには (特定の SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-158">**To configure the Web server (a specific SQL Server)**</span></span>
=======
<span data-ttu-id="bc5c6-159">Web サーバーから特定の SQL Server にアクセスした場合は、web サーバー コンピューターで SQL Server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-159">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="bc5c6-160">特定の SQL Server 接続のネットワーク ライブラリを変更するには、次のように web サーバー コンピューターで SQL Server クライアント ソフトウェアを構成します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-160">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="bc5c6-161">**(特定の SQL Server) の web サーバーを構成するのには**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-161">**To configure the web server (a specific SQL Server)**</span></span>
>>>>>>> <span data-ttu-id="bc5c6-162">master</span><span class="sxs-lookup"><span data-stu-id="bc5c6-162">master</span></span>

<span data-ttu-id="bc5c6-163">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-163">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="bc5c6-164">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 6.5**をポイントし、[ **SQL クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-164">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="bc5c6-165">[**詳細設定**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-165">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="bc5c6-166">[**サーバー** ] ボックスで、 **TCP/IP ソケット**を使用する接続先のサーバーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-166">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="bc5c6-167">[ **DLL 名**] ボックスで、 **TCP/IP ソケット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-167">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="bc5c6-168">**追加/変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-168">Click **Add/Modify**.</span></span> <span data-ttu-id="bc5c6-169">このサーバーをポイントするすべてのデータ ソースが TCP/IP ソケットを使用ようになりました。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-169">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="bc5c6-170">**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-170">Click **Done**.</span></span>

<span data-ttu-id="bc5c6-171">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-171">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="bc5c6-172">**[スタート**] メニューから [**プログラム**] をポイントし、[ **Microsoft SQL Server 7.0**をポイントし、**クライアント設定ユーティリティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-172">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="bc5c6-173">[**全般**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-173">Click the **General** tab.</span></span>

3.  <span data-ttu-id="bc5c6-174">**[追加]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-174">Click **Add**.</span></span>

4.  <span data-ttu-id="bc5c6-175">**サーバー別名**] ボックスで、サーバーの別名を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-175">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="bc5c6-176">[**ネットワーク ライブラリ**] ボックスで、 **TCP/IP**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-176">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="bc5c6-177">[**コンピューター名**] ボックスで、TCP/IP ソケット クライアントをリッスンしているコンピューターのコンピューター名を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-177">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="bc5c6-178">[**ポート番号**] ボックスで、SQL Server がリッスンするポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-178">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="bc5c6-179">**[Ok]**、し **[ok]** もう一度ユーティリティを終了する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc5c6-179">Click **OK**, and then **OK** again to exit the utility.</span></span>

