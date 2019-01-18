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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698156"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="3d59a-102">StartNewWorkflow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="3d59a-102">StartNewWorkflow macro action</span></span>


<span data-ttu-id="3d59a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3d59a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d59a-104">**StartNewWorkflow**アクションを使用すると、リンクされた Microsoft SharePoint Foundation リストに項目の新しいワークフローを開始します。</span><span class="sxs-lookup"><span data-stu-id="3d59a-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="3d59a-105">設定値</span><span class="sxs-lookup"><span data-stu-id="3d59a-105">Setting</span></span>

<span data-ttu-id="3d59a-106">**StartNewWorkflow**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="3d59a-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d59a-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="3d59a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3d59a-108">説明</span><span class="sxs-lookup"><span data-stu-id="3d59a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d59a-109"><strong>Record Number/レコード番号</strong></span><span class="sxs-lookup"><span data-stu-id="3d59a-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="3d59a-110">リストの最初の項目の<strong>1</strong> 、2 番目の<strong>2</strong>項目というように、SharePoint Foundation リスト内の項目の位置。</span><span class="sxs-lookup"><span data-stu-id="3d59a-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="3d59a-111">この引数に式を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d59a-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3d59a-112">解説</span><span class="sxs-lookup"><span data-stu-id="3d59a-112">Remarks</span></span>

  - <span data-ttu-id="3d59a-113">**StartNewWorkflow**アクションでは、**新しいワークフローの開始**] ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d59a-113">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box.</span></span> <span data-ttu-id="3d59a-114">このダイアログ ボックスには、指定した項目で使用可能なすべてのワークフローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d59a-114">This dialog box displays all workflows that are available for the specified item.</span></span> <span data-ttu-id="3d59a-115">このアクションを使用して開始する前に、SharePoint Foundation でリストに対してワークフローを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d59a-115">A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="3d59a-116">**StartNewWorkflow**アクションは、リンクされた SharePoint リストが開かれ、選択した後にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d59a-116">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected.</span></span> <span data-ttu-id="3d59a-117">開き、リンクされたリストを選択するには、 **OpenTable**のアクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d59a-117">To open and select the linked list, use the **OpenTable** action.</span></span> <span data-ttu-id="3d59a-118">リストが既に開いている場合は、 **SelectObject**アクションを使用して選択します。</span><span class="sxs-lookup"><span data-stu-id="3d59a-118">If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="3d59a-119">**StartNewWorkflow**アクションには、データシート ビューで開いている間は、SharePoint リストにリンクされている任意のセルを右クリックし、**ワークフロー**、] をポイントし、[**新しいワークフローの開始**] をクリックと同じ効果があります。</span><span class="sxs-lookup"><span data-stu-id="3d59a-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="3d59a-120">**StartNewWorkflow**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**StartNewWorkflow**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d59a-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

