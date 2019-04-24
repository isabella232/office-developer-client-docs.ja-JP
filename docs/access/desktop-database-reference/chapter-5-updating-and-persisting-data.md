---
title: '第 5 章: データの更新および永続化'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18dd63acd733624fba522ee7382f305d34019905
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296431"
---
# <a name="chapter-5-updating-and-persisting-data"></a><span data-ttu-id="21e4b-102">第 5 章: データの更新および永続化</span><span class="sxs-lookup"><span data-stu-id="21e4b-102">Chapter 5: Updating and persisting data</span></span>

<span data-ttu-id="21e4b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="21e4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21e4b-p101">これまでの章では、ADO を使用してデータ ソース内のデータにアクセスする方法、データ内を移動する方法、およびデータを編集する方法について説明しました。ユーザーがデータを変更できるようにするアプリケーションを構築する場合、これらの変更を保存する方法を理解しておく必要があります。 **Save** メソッドを使用して **Recordset** の変更をファイルに保存することも、 **Update** メソッドまたは **UpdateBatch** メソッドを使用して、変更内容をデータ ソースに返送して保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="21e4b-p101">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data. Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes. You can either persist the **Recordset** changes to a file using the **Save** method, or you can send the changes back to the data source for storage using the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="21e4b-p102">これまでの章では、 **Recordset** の複数の行で変更を行いました。ADO では、データ行の追加、削除、および変更に関連する 2 つの基本的な概念をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="21e4b-p102">In the preceding chapters, you changed the data in several rows of the **Recordset**. ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</span></span>

<span data-ttu-id="21e4b-109">最初の概念は、変更が直ちに**Recordset**に加えられないことです。代わりに、内部*コピーバッファー*に対して行われます。</span><span class="sxs-lookup"><span data-stu-id="21e4b-109">The first notion is that changes aren't immediately made to the **Recordset**; instead, they are made to an internal *copy buffer*.</span></span> <span data-ttu-id="21e4b-110">If you decide you don't want the changes, the modifications in the copy buffer are discarded.</span><span class="sxs-lookup"><span data-stu-id="21e4b-110">If you decide you don't want the changes, the modifications in the copy buffer are discarded.</span></span> <span data-ttu-id="21e4b-111">If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-111">If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span></span>

<span data-ttu-id="21e4b-112">2番目の概念は、変更がデータソースに反映されるのは、行の作業が完了した直後 (つまり*即時*モード)、または一連の行に対するすべての変更が、設定完了の作業を宣言するまで収集される (つまり、、*バッチ*モード)。</span><span class="sxs-lookup"><span data-stu-id="21e4b-112">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, *immediate* mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, *batch* mode).</span></span> <span data-ttu-id="21e4b-113">The **LockType** property determines when the changes are made to the underlying data source.</span><span class="sxs-lookup"><span data-stu-id="21e4b-113">The **LockType** property determines when the changes are made to the underlying data source.</span></span> <span data-ttu-id="21e4b-114">**adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode.</span><span class="sxs-lookup"><span data-stu-id="21e4b-114">**adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode.</span></span> <span data-ttu-id="21e4b-115">The **CursorLocation** property can affect which **LockType** settings are available.</span><span class="sxs-lookup"><span data-stu-id="21e4b-115">The **CursorLocation** property can affect which **LockType** settings are available.</span></span> <span data-ttu-id="21e4b-116">For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-116">For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span></span>

<span data-ttu-id="21e4b-p105">即時モードでは、**Update** メソッドを呼び出すたびに、変更がデータ ソースに反映されます。バッチ モードでは、**Update** を呼び出すか、現在の行の位置が移動されるたびに、変更内容がコピー バッファーに保存されますが、データ ソースに変更を反映するのは **UpdateBatch** メソッドのみです。</span><span class="sxs-lookup"><span data-stu-id="21e4b-p105">In immediate mode, each invocation of the **Update** method propagates the changes to the data source. In batch mode, each invocation of **Update** or movement of the current row position saves the changes to the copy buffer, but only the **UpdateBatch** method propagates the changes to the data source.</span></span>

<span data-ttu-id="21e4b-119">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="21e4b-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="21e4b-120">データを更新する (ADO)</span><span class="sxs-lookup"><span data-stu-id="21e4b-120">Updating data (ADO)</span></span>](updating-data.md)
- [<span data-ttu-id="21e4b-121">データを永続化する (ADO)</span><span class="sxs-lookup"><span data-stu-id="21e4b-121">Persisting data (ADO)</span></span>](persisting-data.md)
