---
title: Before Delete マクロ イベント
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7863f8500a81014f3c70b5547fb363c46803f4f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478458"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="7af80-102">Before Delete マクロ イベント</span><span class="sxs-lookup"><span data-stu-id="7af80-102">Before Delete Macro Event</span></span>

<span data-ttu-id="7af80-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7af80-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7af80-104">**削除する前に**イベントは、レコードが削除されると、変更がコミットされる前に発生します。</span><span class="sxs-lookup"><span data-stu-id="7af80-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="7af80-105">**前に Delete**イベントは、データ マクロでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="7af80-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af80-106">備考</span><span class="sxs-lookup"><span data-stu-id="7af80-106">Remarks</span></span>

<span data-ttu-id="7af80-107">使用して、レコードの前に発生する操作を実行**する前に削除**イベントが削除されます。</span><span class="sxs-lookup"><span data-stu-id="7af80-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="7af80-108">**変更**する前に、検証を実行して、カスタム エラー メッセージが発生する通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="7af80-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="7af80-109">次の構文を使用して、削除するレコードの値にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="7af80-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="7af80-110">など、削除するレコードの QuantityInStock フィールドの値にアクセスするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="7af80-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="7af80-111">**削除する前に**イベントが終了したとき、削除するレコードに含まれる値が完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="7af80-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="7af80-112">**RaiseError**アクションを使用して、**削除する前に**イベントをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="7af80-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="7af80-113">エラーが発生すると**する前に Delete**イベントに含まれる変更は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="7af80-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="7af80-114">**削除する前に**イベントで使用できるマクロのコマンドを次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="7af80-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7af80-115">コマンドの種類</span><span class="sxs-lookup"><span data-stu-id="7af80-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="7af80-116">コマンド</span><span class="sxs-lookup"><span data-stu-id="7af80-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7af80-117">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="7af80-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7af80-118"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="7af80-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7af80-119">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="7af80-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7af80-120"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="7af80-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7af80-121">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="7af80-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="7af80-122"><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="7af80-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7af80-123">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="7af80-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="7af80-124"><a href="lookuprecord-data-block.md">不一致のマクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-124"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7af80-125">データ アクション</span><span class="sxs-lookup"><span data-stu-id="7af80-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7af80-126"><a href="clearmacroerror-macro-action.md">"ClearMacroError/マクロエラーのクリア" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7af80-127">データ アクション</span><span class="sxs-lookup"><span data-stu-id="7af80-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7af80-128"><a href="onerror-macro-action.md">OnError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7af80-129">データ アクション</span><span class="sxs-lookup"><span data-stu-id="7af80-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7af80-130"><a href="raiseerror-macro-action.md">"RaiseError/エラーの生成" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7af80-131">データ アクション</span><span class="sxs-lookup"><span data-stu-id="7af80-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7af80-132"><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7af80-133">データ アクション</span><span class="sxs-lookup"><span data-stu-id="7af80-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="7af80-134"><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="7af80-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7af80-135">**削除する前に**イベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="7af80-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="7af80-136">**削除する前に**イベントをキャプチャするテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="7af80-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="7af80-137">[**表**] タブで、[**前に、のイベント**] を選択**する前に削除**します。</span><span class="sxs-lookup"><span data-stu-id="7af80-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

