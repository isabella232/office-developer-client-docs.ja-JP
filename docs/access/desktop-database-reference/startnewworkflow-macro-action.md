---
title: StartNewWorkflow マクロ アクション
TOCTitle: StartNewWorkflow macro action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1e37d72754531fc4dd51427eefb355a057d08073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306399"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="86744-102">StartNewWorkflow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="86744-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="86744-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="86744-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86744-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span><span class="sxs-lookup"><span data-stu-id="86744-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="86744-105">Setting</span><span class="sxs-lookup"><span data-stu-id="86744-105">Setting</span></span>

<span data-ttu-id="86744-106">"StartNewWorkflow/新しいワークフローの開始" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="86744-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86744-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="86744-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86744-108">説明</span><span class="sxs-lookup"><span data-stu-id="86744-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86744-109"><strong>Record Number/レコード番号</strong></span><span class="sxs-lookup"><span data-stu-id="86744-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="86744-110">SharePoint Foundation リスト内の項目の位置。リストの最初の項目は<strong>1</strong>で、2番目の項目は<strong>2</strong>になります。</span><span class="sxs-lookup"><span data-stu-id="86744-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="86744-111">この引数の式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="86744-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="86744-112">注釈</span><span class="sxs-lookup"><span data-stu-id="86744-112">Remarks</span></span>

  - <span data-ttu-id="86744-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span><span class="sxs-lookup"><span data-stu-id="86744-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="86744-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span><span class="sxs-lookup"><span data-stu-id="86744-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="86744-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span><span class="sxs-lookup"><span data-stu-id="86744-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="86744-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="86744-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

