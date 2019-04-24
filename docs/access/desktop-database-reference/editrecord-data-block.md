---
title: データのレコードの禁止
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293596"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="c8225-102">データのレコードの禁止</span><span class="sxs-lookup"><span data-stu-id="c8225-102">EditRecord data block</span></span>

<span data-ttu-id="c8225-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8225-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8225-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span><span class="sxs-lookup"><span data-stu-id="c8225-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="c8225-105">EditRecord データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c8225-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="c8225-106">Setting</span><span class="sxs-lookup"><span data-stu-id="c8225-106">Setting</span></span>

<span data-ttu-id="c8225-107">**EditRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c8225-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8225-108">引数</span><span class="sxs-lookup"><span data-stu-id="c8225-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="c8225-109">説明</span><span class="sxs-lookup"><span data-stu-id="c8225-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8225-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="c8225-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="c8225-p101">編集するレコードを識別する文字列。"Alias/別名" 引数を指定しない場合、カレント レコードが編集されます。</span><span class="sxs-lookup"><span data-stu-id="c8225-p101">A string that identifies the record to edit. If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c8225-113">注釈</span><span class="sxs-lookup"><span data-stu-id="c8225-113">Remarks</span></span>

<span data-ttu-id="c8225-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span><span class="sxs-lookup"><span data-stu-id="c8225-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8225-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="c8225-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8225-117"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="c8225-117"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8225-118"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="c8225-118"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8225-119"><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。Else マクロステートメント</a></span><span class="sxs-lookup"><span data-stu-id="c8225-119"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8225-120"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="c8225-120"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8225-121"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="c8225-121"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c8225-122">Use the **SetField** action to specify the new values of a field in the edited record.</span><span class="sxs-lookup"><span data-stu-id="c8225-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="c8225-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span><span class="sxs-lookup"><span data-stu-id="c8225-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="c8225-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span><span class="sxs-lookup"><span data-stu-id="c8225-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="c8225-p104">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="c8225-p104">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="c8225-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span><span class="sxs-lookup"><span data-stu-id="c8225-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

