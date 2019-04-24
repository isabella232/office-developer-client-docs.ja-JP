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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312118"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="8119d-102">RDS を ODBC 接続プールと共に使用する</span><span class="sxs-lookup"><span data-stu-id="8119d-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="8119d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8119d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8119d-p101">ODBC データ ソースを使用している場合は、インターネット インフォメーション サービス (IIS) の接続プール オプションを使って、クライアントの読み込みのパフォーマンスを向上できます。接続プールは接続のためのリソース マネージャーで、頻繁に使用される接続を開いた状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="8119d-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="8119d-106">接続プールを有効にする方法については、インターネット インフォメーション サービスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8119d-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="8119d-107">Microsoft インターネットインフォメーションサービスのドキュメントで説明されているように、接続プールを有効にすると、web サーバーに他の制限が適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8119d-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="8119d-108">接続プールの安定性とパフォーマンスの向上を確保するには、TCP/IP ソケット ネットワーク ライブラリを使用するように Microsoft SQL Server を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8119d-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="8119d-109">そのためには、次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="8119d-109">To do this, you need to:</span></span>

  - <span data-ttu-id="8119d-110">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する。</span><span class="sxs-lookup"><span data-stu-id="8119d-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="8119d-111">tcp/ip ソケットを使用するように web サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="8119d-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="8119d-112">TCP/IP ソケットを使用するように SQL Server コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="8119d-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="8119d-113">SQL Server コンピューター上で SQL Server セットアップ プログラムを実行し、データ ソースとの対話に TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="8119d-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="8119d-114">**SQL Server コンピューターで TCP/IP ソケット ネットワーク ライブラリを指定するには**</span><span class="sxs-lookup"><span data-stu-id="8119d-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="8119d-115">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8119d-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span><span class="sxs-lookup"><span data-stu-id="8119d-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="8119d-117">Click **Continue** twice.</span><span class="sxs-lookup"><span data-stu-id="8119d-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="8119d-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span><span class="sxs-lookup"><span data-stu-id="8119d-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="8119d-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="8119d-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="8119d-120">Click **Continue** to finish, and exit setup.</span><span class="sxs-lookup"><span data-stu-id="8119d-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="8119d-121">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8119d-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="8119d-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="8119d-123">On the **General** tab of the dialog box, click **Add**.</span><span class="sxs-lookup"><span data-stu-id="8119d-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="8119d-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="8119d-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="8119d-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span><span class="sxs-lookup"><span data-stu-id="8119d-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="8119d-126">Click **OK** to finish, and exit setup.</span><span class="sxs-lookup"><span data-stu-id="8119d-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="8119d-127">tcp/ip ソケットを使用するように web サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="8119d-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="8119d-128">tcp/ip ソケットを使用するように web サーバーを構成するには、2つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="8119d-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="8119d-129">web サーバーからすべての sql server にアクセスできるかどうか、または web サーバーから特定の sql server だけにアクセスできるかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="8119d-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="8119d-130">すべての sql サーバーが web サーバーからアクセスされている場合は、web サーバーコンピューターで sql server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8119d-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="8119d-131">次の手順では、この IIS web サーバーから作成されたすべての SQL server 接続の既定のネットワークライブラリを変更して、tcp/ip ソケットネットワークライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="8119d-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="8119d-132">**web サーバー (すべての SQL server) を構成するには**</span><span class="sxs-lookup"><span data-stu-id="8119d-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="8119d-133">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8119d-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8119d-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8119d-135">Click the **Net Library** tab.</span><span class="sxs-lookup"><span data-stu-id="8119d-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="8119d-136">In the **Default Network** box, select **TCP/IP Sockets**.</span><span class="sxs-lookup"><span data-stu-id="8119d-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="8119d-137">Click **Done** to save changes and exit the utility.</span><span class="sxs-lookup"><span data-stu-id="8119d-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="8119d-138">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8119d-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="8119d-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="8119d-140">[**General**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8119d-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="8119d-141">In the **Default network library** box, click **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="8119d-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="8119d-142">Click **OK** to save changes and exit the utility.</span><span class="sxs-lookup"><span data-stu-id="8119d-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="8119d-143">web サーバーから特定の sql server にアクセスする場合は、web サーバーコンピューターで sql server クライアント設定ユーティリティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8119d-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="8119d-144">特定の sql server 接続のネットワークライブラリを変更するには、web サーバーコンピューターで sql server クライアントソフトウェアを次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="8119d-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="8119d-145">**web サーバーを構成するには (特定の SQL server)**</span><span class="sxs-lookup"><span data-stu-id="8119d-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="8119d-146">**Microsoft SQL Server 6.5 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="8119d-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8119d-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8119d-148">Click the **Advanced** tab.</span><span class="sxs-lookup"><span data-stu-id="8119d-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="8119d-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span><span class="sxs-lookup"><span data-stu-id="8119d-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="8119d-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span><span class="sxs-lookup"><span data-stu-id="8119d-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="8119d-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="8119d-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="8119d-153">Click **Done**.</span><span class="sxs-lookup"><span data-stu-id="8119d-153">Click **Done**.</span></span>

<span data-ttu-id="8119d-154">**Microsoft SQL Server 7.0 の場合**</span><span class="sxs-lookup"><span data-stu-id="8119d-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="8119d-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="8119d-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="8119d-156">Click the **General** tab.</span><span class="sxs-lookup"><span data-stu-id="8119d-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="8119d-157">Click **Add**.</span><span class="sxs-lookup"><span data-stu-id="8119d-157">Click **Add**.</span></span>

4.  <span data-ttu-id="8119d-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span><span class="sxs-lookup"><span data-stu-id="8119d-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="8119d-162">Click **OK**, and then **OK** again to exit the utility.</span><span class="sxs-lookup"><span data-stu-id="8119d-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

