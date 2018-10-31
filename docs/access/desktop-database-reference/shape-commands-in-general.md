---
title: 一般的な Shape コマンド
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5cf2dc58ee3fa9205b9657366d8706b64b0aa58a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861030"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="fdb1b-102">一般的な Shape コマンド</span><span class="sxs-lookup"><span data-stu-id="fdb1b-102">Shape Commands in General</span></span>


<span data-ttu-id="fdb1b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdb1b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdb1b-104">データ シェイプでは、シェイプされる **Recordset** の列、列で表されるエンティティ間の関係、および **Recordset** にデータを設定する方法を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="fdb1b-105">シェイプされる **Recordset** は、以下のような種類の列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdb1b-106">列の種類</span><span class="sxs-lookup"><span data-stu-id="fdb1b-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="fdb1b-107">説明</span><span class="sxs-lookup"><span data-stu-id="fdb1b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdb1b-108">data</span><span class="sxs-lookup"><span data-stu-id="fdb1b-108">data</span></span></p></td>
<td><p><span data-ttu-id="fdb1b-109">データ プロバイダー、テーブル、または既にシェイプされている <strong>Recordset</strong> に対してクエリ コマンドが返す <strong>Recordset</strong> のフィールド。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdb1b-110">チャプター</span><span class="sxs-lookup"><span data-stu-id="fdb1b-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="fdb1b-111">別の<strong>レコード セット</strong>への参照では、<em>章</em>と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-111">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>.</span></span> <span data-ttu-id="fdb1b-112">チャプター列では、<em></em>親子関係を定義できます。<em></em>親とは、チャプター列を含む<strong>レコードセット</strong>で、<em></em>子とは、チャプターで表される<strong>レコードセット</strong>です。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-112">Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdb1b-113">集計</span><span class="sxs-lookup"><span data-stu-id="fdb1b-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="fdb1b-114">列の値は、すべての行または子<strong>Recordset</strong>のすべての行の列で、<em>集計関数</em>を実行することによって派生します。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-114">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>.</span></span> <span data-ttu-id="fdb1b-115">(次のトピック「<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>」での集計関数を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-115">(See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdb1b-116">演算式</span><span class="sxs-lookup"><span data-stu-id="fdb1b-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="fdb1b-p103">列の値は、<strong>Recordset</strong> の同じ行にある複数の列に対して Visual Basic for Applications の式を実行することで算出されます。式は、CALC 関数への引数です (次のトピック「<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>」および「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」の演算式を参照)。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-p103">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>. The expression is the argument to the CALC function. (See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdb1b-120">新規</span><span class="sxs-lookup"><span data-stu-id="fdb1b-120">new</span></span></p></td>
<td><p><span data-ttu-id="fdb1b-p104">後でデータを入力できるように空の状態で作成されるフィールド。この列は、NEW キーワードで定義されます (次のトピック「<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>」の NEW キーワードを参照)。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-p104">Empty, fabricated fields, which may be populated with data at a later time. The column is defined with the NEW keyword. (See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fdb1b-p105">shape コマンドには、 **Recordset** オブジェクトを返す基のデータ プロバイダーに対してクエリ コマンドを指定するための句を含めることができます。クエリの構文は、基になるデータ プロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は Structured Query Language (SQL) を使用します。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="fdb1b-p106">SQL の JOIN 句を使用して 2 つのテーブルを関連付けることはできますが、階層 **Recordset** を使用すると、さらに効率的に情報を表すことができます。JOIN で作成された **Recordset** の各行には、1 つのテーブルからの情報が冗長的に繰り返し格納されます。階層 **Recordset** では、複数の子 **Recordset** オブジェクトのそれぞれに対して、ただ 1 つの親 **Recordset** が存在します。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-p106">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently. Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables. A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="fdb1b-130"><<<<<<<**レコード セット**オブジェクトまたは[コマンド](command-object-ado.md)オブジェクトの[CommandText](commandtext-property-ado.md)プロパティを設定し、 [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドを呼び出すことによって、ヘッドの図形コマンドを発行できます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-130"><<<<<<< HEAD Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>
<span data-ttu-id="fdb1b-131">===**レコード セット**オブジェクトまたは[コマンド](command-object-ado.md)オブジェクトの[CommandText](commandtext-property-ado.md)プロパティを設定し、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを呼び出すことによって、は、図形のコマンドを発行できます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-131">======= Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>
>>>>>>> <span data-ttu-id="fdb1b-132">master</span><span class="sxs-lookup"><span data-stu-id="fdb1b-132">master</span></span>

<span data-ttu-id="fdb1b-133">shape コマンドはネストできます。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-133">Shape commands can be nested.</span></span> <span data-ttu-id="fdb1b-134">つまり、*親コマンド*または*子コマンド*自体があります別の shape コマンドです。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-134">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="fdb1b-135">shape プロバイダーは、ユーザーが **adUseServer** のカーソル位置を指定した場合でも、常にクライアント カーソルを返します。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-135">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="fdb1b-136">階層 **Recordset** の移動については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-136">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="fdb1b-137">shape コマンドの厳密な構文については、「[正式な Shape 文法](formal-shape-grammar.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdb1b-137">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fdb1b-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="fdb1b-138">See also</span></span>

- [<span data-ttu-id="fdb1b-139">基になるデータ プロバイダーにコマンドを発行する</span><span class="sxs-lookup"><span data-stu-id="fdb1b-139">Issuing Commands to the Underlying Data Provider</span></span>](issuing-commands-to-the-underlying-data-provider.md)

