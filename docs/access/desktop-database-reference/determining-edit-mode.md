---
title: 編集モードを判断する
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53167d7438ecce673fed64f3c7b8d53fbbfbaa5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479517"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="5cc4e-102">編集モードを判断する</span><span class="sxs-lookup"><span data-stu-id="5cc4e-102">Determining Edit Mode</span></span>


<span data-ttu-id="5cc4e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cc4e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5cc4e-p101">ADO では、現在のレコードに関連付けられた編集バッファーが保持されます。 **EditMode** プロパティは、このバッファーに変更が加えられたかどうかや、新しいレコードが作成されたかどうかを示します。 **EditMode** を使用すると、現在のレコードの編集ステータスを判断できます。編集処理が中断された場合に、保留中の変更を確認し、 **Update** メソッドまたは **CancelUpdate** メソッドを使用する必要があるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="5cc4e-108">**EditMode** は、次の表に示す **EditModeEnum** 定数のうちいずれか 1 つを返します。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cc4e-109">定数</span><span class="sxs-lookup"><span data-stu-id="5cc4e-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="5cc4e-110">説明</span><span class="sxs-lookup"><span data-stu-id="5cc4e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc4e-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="5cc4e-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc4e-112">進行中の編集操作がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc4e-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="5cc4e-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc4e-114">現在のレコードのデータが変更されたが、保存されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc4e-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="5cc4e-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc4e-116"><strong>AddNew</strong> メソッドが呼び出されたことを示します。このため、コピー バッファー内の現在のレコードは、データベースに保存されていない新しいレコードです。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc4e-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="5cc4e-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc4e-118">現在のレコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cc4e-p102">**EditMode** が有効な値を返すことができるのは、現在のレコードが存在する場合のみです。 **EditMode** は、 **BOF** または **EOF** が **True** であるか、現在のレコードが削除されている場合には、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="5cc4e-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

