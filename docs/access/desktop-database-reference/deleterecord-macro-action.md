---
title: DeleteRecord マクロ アクション
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 052e7a489eaec526db1552ced89b095f65f652df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921587"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="2b393-102">DeleteRecord マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2b393-102">DeleteRecord macro action</span></span>

<span data-ttu-id="2b393-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2b393-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b393-104">" **DeleteRecord/レコードの削除** " アクションを使用して、レコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="2b393-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="2b393-105">設定</span><span class="sxs-lookup"><span data-stu-id="2b393-105">Setting</span></span>

<span data-ttu-id="2b393-106">**CreateRecord** データ ブロックの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2b393-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b393-107">引数</span><span class="sxs-lookup"><span data-stu-id="2b393-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="2b393-108">説明</span><span class="sxs-lookup"><span data-stu-id="2b393-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b393-109"><strong>Record Alias/レコードの別名</strong></span><span class="sxs-lookup"><span data-stu-id="2b393-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="2b393-110">削除するレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="2b393-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="2b393-111"><em>別名</em>引数を指定しない場合は、現在のレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2b393-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="2b393-112">備考</span><span class="sxs-lookup"><span data-stu-id="2b393-112">Remarks</span></span>

<span data-ttu-id="2b393-p102">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="2b393-p102">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

