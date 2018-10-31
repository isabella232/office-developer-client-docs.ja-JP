---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1779f2c7e16e2f39a3912f271296c6a7bd0fd550
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861947"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="a8465-102">Command オブジェクトを使用する (Access)</span><span class="sxs-lookup"><span data-stu-id="a8465-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="a8465-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8465-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8465-p101">データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="a8465-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="a8465-p102">**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a8465-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="a8465-p103">データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="a8465-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="a8465-114">特定のコマンドは、プロバイダーでサポートされる場合、結果セットのバイナリ ストリームとしてまたは 1 つのレコードとしてではなく、レコード セットを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a8465-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="a8465-115">いくつかのコマンドは結果セットのすべての (SQL Update クエリなど) を取得するものではありません。</span><span class="sxs-lookup"><span data-stu-id="a8465-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="a8465-116">この章では説明の最も一般的なシナリオ、ただし: 結果を返す Recordset オブジェクトにコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a8465-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="a8465-117">レコードまたはストリームに結果を取得する方法の詳細についてを参照してください[第 10 章: レコードとストリーム](chapter-10-records-and-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="a8465-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="a8465-118">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a8465-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="a8465-119">Command オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="a8465-119">Command Object Overview</span></span>](command-object-overview.md)

- [<span data-ttu-id="a8465-120">シンプルなコマンドを作成し、実行する</span><span class="sxs-lookup"><span data-stu-id="a8465-120">Creating and Executing a Simple Command</span></span>](creating-and-executing-a-simple-command.md)

- [<span data-ttu-id="a8465-121">Command オブジェクトのパラメーター</span><span class="sxs-lookup"><span data-stu-id="a8465-121">Command Object Parameters</span></span>](command-object-parameters.md)

- [<span data-ttu-id="a8465-122">Command を使ってストアド プロシージャを呼び出す</span><span class="sxs-lookup"><span data-stu-id="a8465-122">Calling a Stored Procedure with a Command</span></span>](calling-a-stored-procedure-with-a-command.md)

- [<span data-ttu-id="a8465-123">名前の付いたコマンド</span><span class="sxs-lookup"><span data-stu-id="a8465-123">Named Commands</span></span>](named-commands.md)
