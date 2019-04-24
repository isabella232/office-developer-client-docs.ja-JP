---
title: 基本的な RDS プログラミング モデル
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296886"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="efca5-102">基本的な RDS プログラミング モデル</span><span class="sxs-lookup"><span data-stu-id="efca5-102">Basic RDS programming model</span></span>

<span data-ttu-id="efca5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="efca5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="efca5-p101">RDS は、次のような状況にあるクライアント アプリケーションを対象としています。このクライアント アプリケーションでは、サーバー上で実行するプログラムと、目的の情報を返すために必要なパラメーターを指定します。サーバー上で呼び出されたプログラムは、指定されたデータ ソースにアクセスして情報を取得し、必要に応じてそのデータを処理し、結果の情報は使用しやすい形式でクライアント アプリケーションに返します。RDS は、次に示す一連の操作を実行する手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="efca5-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

- <span data-ttu-id="efca5-p102">サーバー上で呼び出すプログラムを指定し、クライアントがそのプログラムを参照する手段を獲得します (この参照は、"プロキシ" とも呼ばれます。これはリモート サーバー プログラムを表します。クライアント アプリケーションは、ローカル プログラムを呼び出すようにプロキシを "呼び出し" ますが、実際にはリモート サーバー プログラムを呼び出します)。</span><span class="sxs-lookup"><span data-stu-id="efca5-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

- <span data-ttu-id="efca5-p103">サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。サーバー プログラムは、実際に ADO を使用してデータ ソースにアクセスします。ADO は、渡されたパラメーターの 1 つを使用して接続し、もう一方のパラメーターに指定されているコマンドを発行します。</span><span class="sxs-lookup"><span data-stu-id="efca5-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

- <span data-ttu-id="efca5-p104">サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。また、 **Recordset** オブジェクトをサーバー上で処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="efca5-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="efca5-117">サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。</span><span class="sxs-lookup"><span data-stu-id="efca5-117">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="efca5-118">クライアントでは、返された **Recordset** オブジェクトを、ビジュアル コントロールで使用しやすい形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="efca5-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="efca5-119">その **Recordset** オブジェクトに変更を加えた場合は、サーバー プログラムに変更が送り返され、その変更がデータ ソースに反映されます。</span><span class="sxs-lookup"><span data-stu-id="efca5-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="efca5-p105">このプログラミング モデルには、便利な機能があります。データ ソースへのアクセスに複雑なサーバー プログラムを必要としない場合は、必要な接続パラメーターおよびコマンド パラメーターを提供すると、自動的に、既定の簡単なサーバー プログラムを使用して指定データを取得できます。</span><span class="sxs-lookup"><span data-stu-id="efca5-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="efca5-p106">複雑な処理が必要な場合は、独自のカスタム サーバー プログラムを指定できます。たとえば、カスタム サーバー プログラムには ADO のすべての機能を自由に組み込むことができるので、複数の異なるデータ ソースに接続し、各データ ソースのデータを複雑な方法で組み合わせて 1 つの単純なデータに加工し、その結果をクライアント アプリケーションに返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="efca5-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="efca5-124">さらに、ADO では、必要に応じて、既定のサーバー プログラムの動作をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="efca5-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

