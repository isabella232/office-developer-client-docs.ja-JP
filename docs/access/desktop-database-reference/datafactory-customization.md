---
title: DataFactory のカスタマイズ
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b805f9d6ff7a1f3b27bb5600d42cabf8fce651cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478893"
---
# <a name="datafactory-customization"></a><span data-ttu-id="12855-102">DataFactory のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="12855-102">DataFactory Customization</span></span>


<span data-ttu-id="12855-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="12855-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="12855-p101">リモート データ サービス (RDS) には、3 階層のクライアント/サーバー システムでデータ アクセスを簡単に行う手段があります。クライアントのデータ コントロールで、リモート データ ソース上でクエリを実行するための接続文字列とコマンド文字列のパラメーターを指定するか、または、更新を実行するための接続文字列と [Recordset](recordset-object-ado.md) オブジェクトのパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="12855-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="12855-p102">パラメーターは、リモート データ ソースでデータ アクセス操作を実行するサーバー プログラムに渡されます。RDS には、[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトという既定のサーバー プログラムがあります。この **RDSServer.DataFactory** は、クエリで作成された **Recordset** オブジェクトをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="12855-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="12855-p103">ただし、 **RDSServer.DataFactory** が実行できるのは、クエリと更新に制限されています。接続文字列またはコマンド文字列の検証または処理は、実行できません。</span><span class="sxs-lookup"><span data-stu-id="12855-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="12855-111">ADO では、 **DataFactory**の作業別の種類のサーバー プログラムと連携して、*ハンドラー*が呼び出されることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="12855-111">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*.</span></span> <span data-ttu-id="12855-112">ハンドラーでは、データ ソースへのアクセスに使用されるようにクライアントの接続文字列とコマンド文字列を変更できます。</span><span class="sxs-lookup"><span data-stu-id="12855-112">The handler can modify client connection and command strings before they are used to access the data source.</span></span> <span data-ttu-id="12855-113">さらに、ハンドラーは、データ ソースにデータを読み書きするクライアントの権限を制御するアクセス権を適用できます。</span><span class="sxs-lookup"><span data-stu-id="12855-113">In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="12855-114">ハンドラーがクライアントのパラメーターとアクセス権の変更に使用するパラメーターは、カスタマイズ ファイルの各セクションに指定します。</span><span class="sxs-lookup"><span data-stu-id="12855-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="12855-115">**DataFactory** オブジェクトのカスタマイズの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="12855-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

  - [<span data-ttu-id="12855-116">カスタマイズ ファイルの概要</span><span class="sxs-lookup"><span data-stu-id="12855-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)

  - [<span data-ttu-id="12855-117">カスタマイズ ファイルの Connect セクション</span><span class="sxs-lookup"><span data-stu-id="12855-117">Customization File Connect Section</span></span>](customization-file-connect-section.md)

  - [<span data-ttu-id="12855-118">カスタマイズ ファイルの SQL セクション</span><span class="sxs-lookup"><span data-stu-id="12855-118">Customization File SQL Section</span></span>](customization-file-sql-section.md)

  - [<span data-ttu-id="12855-119">カスタマイズ ファイルの UserList セクション</span><span class="sxs-lookup"><span data-stu-id="12855-119">Customization File UserList Section</span></span>](customization-file-userlist-section.md)

  - [<span data-ttu-id="12855-120">カスタマイズ ファイルの Logs セクション</span><span class="sxs-lookup"><span data-stu-id="12855-120">Customization File Logs Section</span></span>](customization-file-logs-section.md)

  - <span data-ttu-id="12855-121">[クライアントで必要な設定](https://msdn.microsoft.com/library/ff836356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="12855-121">[Required Client Settings](https://msdn.microsoft.com/library/ff836356\(v=office.15\))</span></span>

  - <span data-ttu-id="12855-122">[カスタマイズした独自のハンドラーを記述する](https://msdn.microsoft.com/library/jj249402\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="12855-122">[Writing Your Own Customized Handler](https://msdn.microsoft.com/library/jj249402\(v=office.15\))</span></span>

