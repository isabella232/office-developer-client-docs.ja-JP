---
title: CreateRecord データ ブロック
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bda30265cbcf2377114734d03b16f889b0d165b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880818"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="aa56d-102">CreateRecord データ ブロック</span><span class="sxs-lookup"><span data-stu-id="aa56d-102">CreateRecord Data Block</span></span>


<span data-ttu-id="aa56d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aa56d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa56d-104">**CreateRecord** データ ブロックを使用して、指定したテーブルに新しいレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="aa56d-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="aa56d-105">[!メモ] **CreateRecord** データ ブロックはデータ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa56d-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="aa56d-106">設定</span><span class="sxs-lookup"><span data-stu-id="aa56d-106">Setting</span></span>

<span data-ttu-id="aa56d-107">**CreateRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="aa56d-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa56d-108">引数</span><span class="sxs-lookup"><span data-stu-id="aa56d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="aa56d-109">必須</span><span class="sxs-lookup"><span data-stu-id="aa56d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="aa56d-110">説明</span><span class="sxs-lookup"><span data-stu-id="aa56d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa56d-111"><strong>内のレコードを作成します。</strong></span><span class="sxs-lookup"><span data-stu-id="aa56d-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="aa56d-112">はい</span><span class="sxs-lookup"><span data-stu-id="aa56d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="aa56d-113">新しいレコードを作成するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="aa56d-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa56d-114"><strong>エイリアス</strong></span><span class="sxs-lookup"><span data-stu-id="aa56d-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="aa56d-115">いいえ</span><span class="sxs-lookup"><span data-stu-id="aa56d-115">No</span></span></p></td>
<td><p><span data-ttu-id="aa56d-p101">レコードを識別する文字列。レコードの別名を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa56d-p101">An string that identifies the record. You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aa56d-118">備考</span><span class="sxs-lookup"><span data-stu-id="aa56d-118">Remarks</span></span>

<span data-ttu-id="aa56d-119">**CreateRecord** で作成したレコードは自動的にカレント レコードになります。</span><span class="sxs-lookup"><span data-stu-id="aa56d-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="aa56d-p102">**CreateRecord** ステートメントの後に、新しいレコードの作成を確定する前に実行するコマンドのブロックを挿入できます。 **CreateRecord** データ ブロックで使用できるアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="aa56d-p102">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed. The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa56d-122"><a href="cancelrecordchange-macro-action.md">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa56d-123"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-123"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa56d-124"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-124"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa56d-125"><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。マクロ ステートメントはその他</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-125"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa56d-126"><a href="setfield-macro-action.md">"SetField/フィールドの設定" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-126"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa56d-127"><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="aa56d-127"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa56d-128">" **CreateRecord** /レコードの作成" アクションでレコードを作成した後、" **SetField** /フィールドの設定" アクションを使用して、新しいレコードのフィールド値を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa56d-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="aa56d-129">場合、**を使用することができます.そうしたら。。。他**の条件に基づいて、ステートメントを使用して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="aa56d-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="aa56d-p103">レコードの作成を取り消すには " **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **CreateRecord** データ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="aa56d-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="aa56d-p104">新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="aa56d-p104">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="aa56d-134">**CreateRecord**データ ブロックは、**[後に挿入](after-insert-macro-event.md)**、**[更新した後](after-update-macro-event.md)**、および**[更新後](after-update-macro-event.md)** のデータ マクロのイベントでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="aa56d-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

