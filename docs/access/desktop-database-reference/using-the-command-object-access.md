---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476671"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="3c8c5-102">Command オブジェクトを使用する (Access)</span><span class="sxs-lookup"><span data-stu-id="3c8c5-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="3c8c5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c8c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3c8c5-p101">データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3c8c5-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="3c8c5-p102">**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c8c5-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="3c8c5-p103">データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="3c8c5-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3c8c5-p104">プロバイダーがサポートしている場合、特定の <STRONG>Command</STRONG> は、結果セットを <STRONG>Recordset</STRONG> としてではなく、バイナリ ストリームまたは 1 つの <STRONG>Record</STRONG> として返すことができます。また、結果セットをまったく返さない <STRONG>Command</STRONG> もあります (SQL Update クエリなど)。ただし、この章では、<STRONG>Recordset</STRONG> オブジェクトに結果を返す <STRONG>Command</STRONG> の実行という最も一般的なシナリオについて説明します。結果を <STRONG>Record</STRONG> または <STRONG>Stream</STRONG> に返す方法の詳細については、「<A href="chapter-10-records-and-streams.md">10 章: レコードとストリーム</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c8c5-p104">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider. Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query). This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object. For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


