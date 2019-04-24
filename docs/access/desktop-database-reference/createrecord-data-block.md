---
title: CreateRecord データブロック
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295353"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="0b48f-102">CreateRecord データブロック</span><span class="sxs-lookup"><span data-stu-id="0b48f-102">CreateRecord data block</span></span>


<span data-ttu-id="0b48f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b48f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b48f-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span><span class="sxs-lookup"><span data-stu-id="0b48f-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="0b48f-105">**CreateRecord** データ ブロックはデータ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b48f-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0b48f-106">Setting</span><span class="sxs-lookup"><span data-stu-id="0b48f-106">Setting</span></span>

<span data-ttu-id="0b48f-107">CreateRecord データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0b48f-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b48f-108">引数</span><span class="sxs-lookup"><span data-stu-id="0b48f-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0b48f-109">必須</span><span class="sxs-lookup"><span data-stu-id="0b48f-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0b48f-110">説明</span><span class="sxs-lookup"><span data-stu-id="0b48f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b48f-111"><strong>Create a Record In</strong>/レコードの作成先</span><span class="sxs-lookup"><span data-stu-id="0b48f-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="0b48f-112">はい</span><span class="sxs-lookup"><span data-stu-id="0b48f-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0b48f-113">新しいレコードを作成するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="0b48f-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b48f-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="0b48f-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="0b48f-115">いいえ</span><span class="sxs-lookup"><span data-stu-id="0b48f-115">No</span></span></p></td>
<td><p><span data-ttu-id="0b48f-p101">レコードを識別する文字列。レコードの別名を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b48f-p101">An string that identifies the record. You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0b48f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="0b48f-118">Remarks</span></span>

<span data-ttu-id="0b48f-119">**CreateRecord** で作成したレコードは自動的にカレント レコードになります。</span><span class="sxs-lookup"><span data-stu-id="0b48f-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="0b48f-p102">**CreateRecord** ステートメントの後に、新しいレコードの作成を確定する前に実行するコマンドのブロックを挿入できます。 **CreateRecord** データ ブロックで使用できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0b48f-p102">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed. The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b48f-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b48f-123"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b48f-124"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b48f-125"><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。Else マクロステートメント</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b48f-126"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b48f-127"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="0b48f-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b48f-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span><span class="sxs-lookup"><span data-stu-id="0b48f-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="0b48f-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span><span class="sxs-lookup"><span data-stu-id="0b48f-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="0b48f-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span><span class="sxs-lookup"><span data-stu-id="0b48f-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="0b48f-p104">新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="0b48f-p104">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="0b48f-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span><span class="sxs-lookup"><span data-stu-id="0b48f-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

