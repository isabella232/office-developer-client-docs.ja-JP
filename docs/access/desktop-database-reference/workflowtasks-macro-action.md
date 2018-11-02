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
ms.openlocfilehash: f22d1a30a2dc7de003510f54d64fcafc9f0f7878
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920208"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="e4987-102">WorkflowTasks マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="e4987-102">WorkflowTasks macro action</span></span>


<span data-ttu-id="e4987-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e4987-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4987-104">**WorkflowTasks**アクションを使用するには、[**ワークフロー タスク**] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e4987-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="e4987-105">設定値</span><span class="sxs-lookup"><span data-stu-id="e4987-105">Setting</span></span>

<span data-ttu-id="e4987-106">**WorkflowTasks**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="e4987-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4987-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="e4987-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e4987-108">説明</span><span class="sxs-lookup"><span data-stu-id="e4987-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4987-109"><strong>Record Number/レコード番号</strong></span><span class="sxs-lookup"><span data-stu-id="e4987-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="e4987-110">リストの最初の項目の<strong>1</strong> 、2 番目の<strong>2</strong>項目というように、Microsoft SharePoint Foundation リスト内の項目の位置。</span><span class="sxs-lookup"><span data-stu-id="e4987-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="e4987-111">この引数に式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="e4987-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e4987-112">解説</span><span class="sxs-lookup"><span data-stu-id="e4987-112">Remarks</span></span>

  - <span data-ttu-id="e4987-113">**WorkflowTasks**アクションは、 **[ワークフロー タスク**] ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4987-113">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box.</span></span> <span data-ttu-id="e4987-114">このダイアログ ボックスは、指定した項目で使用可能なすべてのタスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="e4987-114">This dialog box displays all tasks that are available for the specified item.</span></span> <span data-ttu-id="e4987-115">SharePoint Foundation でリストに対してワークフローを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4987-115">A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="e4987-116">**WorkflowTasks**アクションは、リンクされた SharePoint Foundation リストが開かれ、選択した後にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4987-116">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected.</span></span> <span data-ttu-id="e4987-117">開き、リンクされたリストを選択するには、 **OpenTable**のアクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4987-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="e4987-118">リストが既に開いている場合は、 **SelectObject**アクションを使用して選択します。</span><span class="sxs-lookup"><span data-stu-id="e4987-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="e4987-119">**WorkflowTasks**アクションは、データシート ビューで開いている間にリンクされている SharePoint Foundation リスト内の任意のセルを右クリックし、**ワークフロー**、] をポイントして、**ワークフローのタスク**をクリックと同じです。</span><span class="sxs-lookup"><span data-stu-id="e4987-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="e4987-120">VBA モジュールでは、 **WorkflowTasks**アクションを実行するには、 **DoCmd**オブジェクトの**WorkflowTasks**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4987-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

