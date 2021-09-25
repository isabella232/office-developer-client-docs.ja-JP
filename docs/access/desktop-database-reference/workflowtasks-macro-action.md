---
title: WorkflowTasks マクロ アクション
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 97c5c3bd337785e4222655538310a194ee45e8cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593285"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks マクロ アクション


**適用先**: Access 2013、Office 2013

You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.

## <a name="setting"></a>設定

"WorkflowTasks/ワークフロータスク" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Record Number/レコード番号</strong></p></td>
<td><p>Microsoft SharePoint Foundation リスト内のアイテムの位置(リストの最初のアイテムは<strong>1、2</strong>番目のアイテムは<strong>2</strong>など)。 また、この引数の式を入力できます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

  - The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.

  - The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.

  - The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.

  - To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.

