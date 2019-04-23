---
title: 非パラメーター化コマンドの操作
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288267"
---
# <a name="operation-of-non-parameterized-commands"></a><span data-ttu-id="ed287-102">非パラメーター化コマンドの操作</span><span class="sxs-lookup"><span data-stu-id="ed287-102">Operation of non-parameterized commands</span></span>


<span data-ttu-id="ed287-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed287-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed287-p101">非パラメーター化コマンドの場合、すべてのプロバイダー コマンドが実行され、コマンドの実行中に **Recordset** が作成されます。コマンドが同期的に実行される場合、すべての **Recordset** が完全に作成されます。非同期作成モードが選択された場合、 **Recordset** の作成状態は、作成モードと **Recordset** のサイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ed287-p101">For non-parameterized commands, all of the provider commands are executed and the **Recordsets** are created during command execution. If the command is executed synchronously, all of the **Recordsets** will be fully populated. If an asynchronous population mode was selected, the populated state of the **Recordsets** will depend on the population mode and the size of the **Recordsets**.</span></span>

<span data-ttu-id="ed287-107">たとえば、*parent-command* は、Customers テーブルからある会社の顧客の **Recordset** を返すことができ、*child-command* は、Orders テーブルからすべての顧客の受注の **Recordset** を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="ed287-107">For example, the *parent-command* could return a **Recordset** of customers for a company from a Customers table, and the *child-command* could return a **Recordset** of orders for all customers from an Orders table.</span></span>

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

<span data-ttu-id="ed287-108">非パラメーター化親子関係の場合、親と子の **Recordset** オブジェクトには、それぞれを関連付ける共通の列が必要です。</span><span class="sxs-lookup"><span data-stu-id="ed287-108">For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them.</span></span> <span data-ttu-id="ed287-109">列の名前は RELATE 句で、まず *parent-column* を、次に *child-column* を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed287-109">The columns are named in the RELATE clause, *parent-column* first and then *child-column*.</span></span> <span data-ttu-id="ed287-110">列の名前は、 **Recordset** オブジェクトごとに異なってもかまいませんが、意味のある関係を指定するために、同じ情報を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed287-110">The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation.</span></span> <span data-ttu-id="ed287-111">たとえば、 **Customers** と **Orders** の両方の **Recordset** オブジェクトに customerID フィールドがある場合などです。</span><span class="sxs-lookup"><span data-stu-id="ed287-111">For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field.</span></span> <span data-ttu-id="ed287-112">子 **Recordset** のメンバーシップはプロバイダー コマンドによって決定されるため、子 **Recordset** に孤立行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ed287-112">Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows.</span></span> <span data-ttu-id="ed287-113">これらの孤立行にアクセスするには、さらにリシェイプを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed287-113">These orphaned rows are inaccessible without further reshaping.</span></span>

<span data-ttu-id="ed287-p103">データ シェイプにより、チャプター列が親 **Recordset** に追加されます。チャプター列の値は、RELATE 句を満たす子 **Recordset** 内の行への参照です。つまり、特定の親行の *parent-column* と、チャプター子のすべての行の *child-column* が同じ値になります。同じ RELATE 句で複数の TO 句が使用される場合、暗黙的に AND 演算子を使用して結合されます。RELATE 句の親列が親 **Recordset** へのキーの構成要素でない場合、1 つの子行に複数の親行が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ed287-p103">Data shaping appends a chapter column to the parent **Recordset**. The values in the chapter column are references to rows in the child **Recordset**, which satisfy the RELATE clause. That is, the same value is in the *parent-column* of a given parent row as is in the *child-column* of all the rows of the chapter child. When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator. If the parent columns in the relate clause do not constitute a key to the parent **Recordset**, a single child row may have multiple parent rows.</span></span>

<span data-ttu-id="ed287-p104">チャプター列の参照にアクセスすると、その参照で表される **Recordset** が ADO によって自動的に取得されます。非パラメーター化コマンドの場合、子 **Recordset** 全体が取得されても、チャプターは行のサブセットのみを表します。</span><span class="sxs-lookup"><span data-stu-id="ed287-p104">When you access the reference in the chapter column, ADO automatically retrieves the **Recordset** represented by the reference. Note that in a non-parameterized command, although the entire child **Recordset** has been retrieved, the chapter only presents a subset of rows.</span></span>

<span data-ttu-id="ed287-p105">追加された列に *chapter-alias* がない場合、その列に対して名前が自動的に生成されます。列の [Field](field-object-ado.md) オブジェクトが **Recordset** オブジェクトの [Fields](fields-collection-ado.md) コレクションに追加され、データ型は **adChapter** になります。</span><span class="sxs-lookup"><span data-stu-id="ed287-p105">If the appended column has no *chapter-alias*, a name will be generated for it automatically. A [Field](field-object-ado.md) object for the column will be appended to the **Recordset** object's [Fields](fields-collection-ado.md) collection, and its data type will be **adChapter**.</span></span>

<span data-ttu-id="ed287-123">階層 **Recordset** の移動については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed287-123">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

