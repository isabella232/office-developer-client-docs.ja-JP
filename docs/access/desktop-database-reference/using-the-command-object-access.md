---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709328"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="d1923-102">コマンド オブジェクト (Access) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="d1923-102">Using the Command object (Access)</span></span>


<span data-ttu-id="d1923-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d1923-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1923-p101">データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="d1923-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="d1923-p102">**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d1923-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="d1923-p103">データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="d1923-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="d1923-114">特定のコマンドは、プロバイダーでサポートされる場合、結果セットのバイナリ ストリームとしてまたは 1 つのレコードとしてではなく、レコード セットを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d1923-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="d1923-115">いくつかのコマンドは結果セットのすべての (SQL Update クエリなど) を取得するものではありません。</span><span class="sxs-lookup"><span data-stu-id="d1923-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="d1923-116">この章では説明の最も一般的なシナリオ、ただし: 結果を返す Recordset オブジェクトにコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d1923-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="d1923-117">レコードまたはストリームに結果を取得する方法の詳細についてを参照してください[第 10 章: レコードとストリーム](chapter-10-records-and-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="d1923-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="d1923-118">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1923-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="d1923-119">Command オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="d1923-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="d1923-120">簡単なコマンドの作成と実行</span><span class="sxs-lookup"><span data-stu-id="d1923-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="d1923-121">Command オブジェクトのパラメーター</span><span class="sxs-lookup"><span data-stu-id="d1923-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="d1923-122">コマンドを使用したストアド プロシージャの呼び出し</span><span class="sxs-lookup"><span data-stu-id="d1923-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="d1923-123">名前付きコマンド</span><span class="sxs-lookup"><span data-stu-id="d1923-123">Named commands</span></span>](named-commands.md)
