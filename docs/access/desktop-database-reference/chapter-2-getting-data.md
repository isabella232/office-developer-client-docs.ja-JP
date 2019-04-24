---
title: '第 2 章: データの取得'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296445"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="21c81-102">第 2 章: データの取得</span><span class="sxs-lookup"><span data-stu-id="21c81-102">Chapter 2: Getting data</span></span>

<span data-ttu-id="21c81-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="21c81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21c81-p101">前の章では、ADO アプリケーションの作成に必要となる、データの取得、データの確認、データの編集、およびデータの更新という 4 つの主な操作について概説しました。この章では、最初の操作であるデータの取得に関連する概念の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="21c81-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="21c81-p102">この操作では、いくつかの ADO オブジェクトが一定の役割を果たします。まず、ADO **Connection** オブジェクトを使用して、データ ソースに接続します (このオブジェクトは暗黙的に作成される場合があります)。次に、ADO **Command** オブジェクトを使用して、実行内容に関する指示をデータ ソースに渡します (このオブジェクトも暗黙的に作成される場合があります)。データ ソースにコマンドを渡し、その応答を受信した結果は、通常、ADO **Recordset** オブジェクトとして表されます。</span><span class="sxs-lookup"><span data-stu-id="21c81-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="21c81-p103">データを取得するには、アプリケーションがデータ ソース (DBMS、ファイル ストア、コンマ区切りテキスト ファイルなど) と通信できる状態にある必要があります。この通信とは、"接続"、つまりデータのやり取りに必要な環境を指します。</span><span class="sxs-lookup"><span data-stu-id="21c81-p103">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file. This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="21c81-p104">ADO のオブジェクト モデルでは、接続の概念を **Connection** オブジェクトで表します。これは、ADO の多くの機能の基盤となるものです。 **Connection** オブジェクトの目的は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="21c81-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

- <span data-ttu-id="21c81-114">ADO が、データ ソースと通信し、セッションを確立するために必要な情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="21c81-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

- <span data-ttu-id="21c81-115">セッションのトランザクション機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="21c81-115">Define the transactional capabilities of the session.</span></span>

- <span data-ttu-id="21c81-116">コマンドを作成し、データ ソースに対して実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="21c81-116">Allow you to create and execute commands against the data source.</span></span>

- <span data-ttu-id="21c81-p105">基になるデータ ソースのデザインに関する情報をスキーマ行セットの形で提供します。スキーマ行セットの詳細については、「[OpenSchema メソッド (ADO)](openschema-method-ado.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21c81-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="21c81-119">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="21c81-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="21c81-120">接続の作成</span><span class="sxs-lookup"><span data-stu-id="21c81-120">Making a connection</span></span>](making-a-connection.md)
- [<span data-ttu-id="21c81-121">connection オブジェクト参照 (ADO) の使用</span><span class="sxs-lookup"><span data-stu-id="21c81-121">Using the connection object reference (ADO)</span></span>](using-the-connection-object-access.md)
- [<span data-ttu-id="21c81-122">command オブジェクト参照 (ADO) の使用</span><span class="sxs-lookup"><span data-stu-id="21c81-122">Using the command object reference (ADO)</span></span>](using-the-command-object-access.md)
- [<span data-ttu-id="21c81-123">Recordset にデータを追加する (ADO)</span><span class="sxs-lookup"><span data-stu-id="21c81-123">Adding data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)
