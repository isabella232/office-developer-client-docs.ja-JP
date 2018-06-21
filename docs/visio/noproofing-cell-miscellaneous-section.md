---
title: NoProofing セル ([その他] セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペル チェックが自動的に修正されたかどうかと、選択した図形のスペル ミスを表示するかどうかを決定します。 ブール値を受け取ります。
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19805924"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="71673-104">NoProofing セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="71673-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="71673-105">スペル チェックが自動的に修正されたかどうかと、選択した図形のスペル ミスを表示するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="71673-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="71673-106">**ブール**値を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="71673-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="71673-107">**値**</span><span class="sxs-lookup"><span data-stu-id="71673-107">**Value**</span></span>|<span data-ttu-id="71673-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="71673-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71673-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="71673-109">TRUE</span></span>  <br/> |<span data-ttu-id="71673-110">スペル チェックが自動的に修正されないと、選択した図形のスペル チェックのエラーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="71673-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="71673-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="71673-111">FALSE</span></span>  <br/> |<span data-ttu-id="71673-112">スペル チェックが自動的に修正され、選択した図形のスペル チェックのエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="71673-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71673-113">備考</span><span class="sxs-lookup"><span data-stu-id="71673-113">Remarks</span></span>

<span data-ttu-id="71673-114">取得する NoProofing] セルへの参照名を別の数式からまたはプログラムでは、 **CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="71673-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71673-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="71673-115">Cell name:</span></span>  <br/> |<span data-ttu-id="71673-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="71673-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="71673-117">プログラムから、インデックスによって [NoProofing] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="71673-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71673-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="71673-118">Section index:</span></span>  <br/> |<span data-ttu-id="71673-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71673-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="71673-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="71673-120">Row index:</span></span>  <br/> |<span data-ttu-id="71673-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="71673-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="71673-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="71673-122">Cell index:</span></span>  <br/> |<span data-ttu-id="71673-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="71673-123">**visObjNoProofing**</span></span> <br/> |
   

