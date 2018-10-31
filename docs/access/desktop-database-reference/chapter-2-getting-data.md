---
title: '第 2 章: データの取得'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 601d18373f5bcd0a9ed6777fa50c2a3ed631594a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860890"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="74c21-102">第 2 章: データの取得</span><span class="sxs-lookup"><span data-stu-id="74c21-102">Chapter 2: Getting Data</span></span>


<span data-ttu-id="74c21-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="74c21-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="74c21-p101">前の章では、ADO アプリケーションの作成に必要となる、データの取得、データの確認、データの編集、およびデータの更新という 4 つの主な操作について概説しました。この章では、最初の操作であるデータの取得に関連する概念の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="74c21-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="74c21-p102">この操作では、いくつかの ADO オブジェクトが一定の役割を果たします。まず、ADO **Connection** オブジェクトを使用して、データ ソースに接続します (このオブジェクトは暗黙的に作成される場合があります)。次に、ADO **Command** オブジェクトを使用して、実行内容に関する指示をデータ ソースに渡します (このオブジェクトも暗黙的に作成される場合があります)。データ ソースにコマンドを渡し、その応答を受信した結果は、通常、ADO **Recordset** オブジェクトとして表されます。</span><span class="sxs-lookup"><span data-stu-id="74c21-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="74c21-110">データを取得するには、アプリケーションは、DBMS、ファイル ストア、コンマ区切りテキスト ファイルなど、データ ソースとの通信にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74c21-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="74c21-111">この通信*接続*とは、データを交換するために必要な環境。</span><span class="sxs-lookup"><span data-stu-id="74c21-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="74c21-p104">ADO のオブジェクト モデルでは、接続の概念を **Connection** オブジェクトで表します。これは、ADO の多くの機能の基盤となるものです。 **Connection** オブジェクトの目的は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74c21-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

  - <span data-ttu-id="74c21-114">ADO が、データ ソースと通信し、セッションを確立するために必要な情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="74c21-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

  - <span data-ttu-id="74c21-115">セッションのトランザクション機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="74c21-115">Define the transactional capabilities of the session.</span></span>

  - <span data-ttu-id="74c21-116">コマンドを作成し、データ ソースに対して実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="74c21-116">Allow you to create and execute commands against the data source.</span></span>

  - <span data-ttu-id="74c21-p105">基になるデータ ソースのデザインに関する情報をスキーマ行セットの形で提供します。スキーマ行セットの詳細については、「[OpenSchema メソッド (ADO)](openschema-method-ado.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74c21-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="74c21-119">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="74c21-119">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="74c21-120">接続を作成する</span><span class="sxs-lookup"><span data-stu-id="74c21-120">Making a Connection</span></span>](making-a-connection.md)

  - [<span data-ttu-id="74c21-121">Connection オブジェクトの使用のリファレンス (ADO)</span><span class="sxs-lookup"><span data-stu-id="74c21-121">Using the Connection Object Reference (ADO)</span></span>](using-the-connection-object-access.md)

  - [<span data-ttu-id="74c21-122">Command オブジェクトの使用のリファレンス (ADO)</span><span class="sxs-lookup"><span data-stu-id="74c21-122">Using the Command Object Reference (ADO)</span></span>](using-the-command-object-access.md)

  - [<span data-ttu-id="74c21-123">レコードセットにデータを追加する (ADO)</span><span class="sxs-lookup"><span data-stu-id="74c21-123">Adding Data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)