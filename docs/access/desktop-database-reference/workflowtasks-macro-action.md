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
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306007"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="76606-102">WorkflowTasks マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="76606-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="76606-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="76606-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76606-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span><span class="sxs-lookup"><span data-stu-id="76606-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="76606-105">Setting</span><span class="sxs-lookup"><span data-stu-id="76606-105">Setting</span></span>

<span data-ttu-id="76606-106">"WorkflowTasks/ワークフロータスク" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="76606-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76606-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="76606-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="76606-108">説明</span><span class="sxs-lookup"><span data-stu-id="76606-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76606-109"><strong>Record Number/レコード番号</strong></span><span class="sxs-lookup"><span data-stu-id="76606-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="76606-110">Microsoft SharePoint Foundation リスト内の項目の位置。リストの最初の項目は<strong>1</strong>で、2番目の項目は<strong>2</strong>になります。</span><span class="sxs-lookup"><span data-stu-id="76606-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="76606-111">この引数の式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="76606-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="76606-112">注釈</span><span class="sxs-lookup"><span data-stu-id="76606-112">Remarks</span></span>

  - <span data-ttu-id="76606-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="76606-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="76606-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span><span class="sxs-lookup"><span data-stu-id="76606-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="76606-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span><span class="sxs-lookup"><span data-stu-id="76606-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="76606-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="76606-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

