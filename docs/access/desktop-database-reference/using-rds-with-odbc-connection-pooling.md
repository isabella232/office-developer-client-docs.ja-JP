---
title: RDS を ODBC 接続プールと共に使用する
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 95111c2698fd6a2efd85a889fcc2a3b40691e68f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572663"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>RDS を ODBC 接続プールと共に使用する


**適用先:** Access 2013、Office 2013

ODBC データ ソースを使用している場合は、インターネット インフォメーション サービス (IIS) の接続プール オプションを使って、クライアントの読み込みのパフォーマンスを向上できます。接続プールは接続のためのリソース マネージャーで、頻繁に使用される接続を開いた状態に保つことができます。

接続プールを有効にする方法については、インターネット インフォメーション サービスのドキュメントを参照してください。

接続プールを有効にすると、Web サーバーに他の制限が適用される場合があります(詳細については、Microsoft インターネット インフォメーション サービスしてください。

接続プールの安定性とパフォーマンスの向上を確保するには、TCP/IP ソケット ネットワーク ライブラリを使用するように Microsoft SQL Server を構成する必要があります。

そのためには、次の作業を行います。

  - TCP/IP ソケットを使用するように SQL Server コンピューターを構成する。

  - TCP/IP ソケットを使用する Web サーバーを構成します。

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>TCP/IP ソケットを使用するように SQL Server コンピューターを構成する

SQL Server コンピューター上で SQL Server セットアップ プログラムを実行し、データ ソースとの対話に TCP/IP ソケット ネットワーク ライブラリを使用するように構成します。

**SQL Server コンピューターで TCP/IP ソケット ネットワーク ライブラリを指定するには**

**Microsoft SQL Server 6.5 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.

2.  Click **Continue** twice.

3.  In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.

4.  Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.

5.  Click **Continue** to finish, and exit setup.

**Microsoft SQL Server 7.0 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.

2.  On the **General** tab of the dialog box, click **Add**.

3.  In the **Add Network Library Configuration** dialog box, click **TCP/IP**.

4.  In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.

5.  Click **OK** to finish, and exit setup.

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>TCP/IP ソケットを使用するための Web サーバーの構成

TCP/IP ソケットを使用する Web サーバーを構成するには、2 つのオプションがあります。 実行する操作は、すべての SQL サーバーが Web サーバーからアクセスされるのか、または web サーバーから特定のサーバー SQL Serverアクセスするかによって異なります。

すべてのサーバー SQL Web サーバーからアクセスする場合は、web サーバー コンピューターで SQL Server クライアント構成ユーティリティを実行する必要があります。 次の手順では、この IIS Web サーバーからSQL Server接続しているすべてのネットワーク ライブラリの既定のネットワーク ライブラリを、TCP/IP Sockets ネットワーク ライブラリを使用するために変更します。

**Web サーバーを構成するには (すべてのサーバー SQL)**

**Microsoft SQL Server 6.5 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.

2.  Click the **Net Library** tab.

3.  In the **Default Network** box, select **TCP/IP Sockets**.

4.  Click **Done** to save changes and exit the utility.

**Microsoft SQL Server 7.0 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.

2.  Click the **General** tab.

3.  In the **Default network library** box, click **TCP/IP**.

4.  Click **OK** to save changes and exit the utility.

特定のサーバー SQL Server Web サーバーからアクセスする場合は、web サーバー コンピューターで SQL Server クライアント構成ユーティリティを実行する必要があります。 特定のクライアント接続のネットワーク ライブラリをSQL Server、web サーバー コンピューター SQL Serverクライアント ソフトウェアを次のように構成します。

**Web サーバーを構成するには (特定のSQL Server)**

**Microsoft SQL Server 6.5 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.

2.  Click the **Advanced** tab.

3.  In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.

4.  In the **DLL Name** box, select **TCP/IP Sockets**.

5.  Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.

6.  Click **Done**.

**Microsoft SQL Server 7.0 の場合**

1.  From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.

2.  Click the **General** tab.

3.  Click **Add**.

4.  Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.

5.  Click **OK**, and then **OK** again to exit the utility.

