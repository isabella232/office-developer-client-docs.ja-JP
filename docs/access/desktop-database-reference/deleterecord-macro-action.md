---
title: "\"DeleteRecord/レコードの削除\" マクロ アクション"
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 536369082a5abb94914d78d8bc64c5f9b45e8b0d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478438"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="1a577-102">"DeleteRecord/レコードの削除" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="1a577-102">DeleteRecord Macro Action</span></span>

<span data-ttu-id="1a577-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a577-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1a577-104">" **DeleteRecord/レコードの削除** " アクションを使用して、レコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="1a577-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="1a577-105">設定</span><span class="sxs-lookup"><span data-stu-id="1a577-105">Setting</span></span>

<span data-ttu-id="1a577-106">**CreateRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1a577-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a577-107">引数</span><span class="sxs-lookup"><span data-stu-id="1a577-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="1a577-108">説明</span><span class="sxs-lookup"><span data-stu-id="1a577-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a577-109"><strong>Record Alias/レコードの別名</strong></span><span class="sxs-lookup"><span data-stu-id="1a577-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="1a577-110">削除するレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="1a577-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="1a577-111"><em>別名</em>引数を指定しない場合は、現在のレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1a577-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="1a577-112">備考</span><span class="sxs-lookup"><span data-stu-id="1a577-112">Remarks</span></span>

<span data-ttu-id="1a577-p102">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="1a577-p102">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

