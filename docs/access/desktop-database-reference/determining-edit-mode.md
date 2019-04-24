---
title: 編集モードを決定する
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293918"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="705d9-102">編集モードを決定する</span><span class="sxs-lookup"><span data-stu-id="705d9-102">Determining Edit mode</span></span>


<span data-ttu-id="705d9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="705d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="705d9-p101">ADO では、現在のレコードに関連付けられた編集バッファーが保持されます。 **EditMode** プロパティは、このバッファーに変更が加えられたかどうかや、新しいレコードが作成されたかどうかを示します。 **EditMode** を使用すると、現在のレコードの編集ステータスを判断できます。編集処理が中断された場合に、保留中の変更を確認し、 **Update** メソッドまたは **CancelUpdate** メソッドを使用する必要があるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="705d9-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="705d9-108">**EditMode** は、次の表に示す **EditModeEnum** 定数のうちいずれか 1 つを返します。</span><span class="sxs-lookup"><span data-stu-id="705d9-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="705d9-109">定数</span><span class="sxs-lookup"><span data-stu-id="705d9-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="705d9-110">説明</span><span class="sxs-lookup"><span data-stu-id="705d9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705d9-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="705d9-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="705d9-112">進行中の編集操作がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="705d9-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705d9-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="705d9-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="705d9-114">現在のレコードのデータが変更されたが、保存されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="705d9-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705d9-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="705d9-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="705d9-116"><strong>AddNew</strong> メソッドが呼び出されたことを示します。このため、コピー バッファー内の現在のレコードは、データベースに保存されていない新しいレコードです。</span><span class="sxs-lookup"><span data-stu-id="705d9-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705d9-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="705d9-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="705d9-118">現在のレコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="705d9-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="705d9-p102">**EditMode** が有効な値を返すことができるのは、現在のレコードが存在する場合のみです。 **EditMode** は、 **BOF** または **EOF** が **True** であるか、現在のレコードが削除されている場合には、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="705d9-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

