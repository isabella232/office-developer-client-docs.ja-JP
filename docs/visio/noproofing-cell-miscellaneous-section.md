---
title: '[NoProofing] セル ([その他] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペルが自動的に修正されるかどうか、および選択した図形にスペル ミスが表示されるかどうかを指定します。 ブール値を取得します。
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431254"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="2f2dc-104">[NoProofing] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="2f2dc-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="2f2dc-105">スペルが自動的に修正されるかどうか、および選択した図形にスペル ミスが表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="2f2dc-106">ブール値 **を取得** します。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="2f2dc-107">**値**</span><span class="sxs-lookup"><span data-stu-id="2f2dc-107">**Value**</span></span>|<span data-ttu-id="2f2dc-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="2f2dc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f2dc-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="2f2dc-109">TRUE</span></span>  <br/> |<span data-ttu-id="2f2dc-110">スペル は自動的に修正されません。選択した図形のスペル ミスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="2f2dc-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="2f2dc-111">FALSE</span></span>  <br/> |<span data-ttu-id="2f2dc-112">スペルが自動的に修正され、選択した図形のスペル ミスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f2dc-113">注釈</span><span class="sxs-lookup"><span data-stu-id="2f2dc-113">Remarks</span></span>

<span data-ttu-id="2f2dc-114">CellsU プロパティを使用して、別の数式またはプログラムから名前によって [NoProofing] セルへの参照を取得するには、次の値を **使用** します。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f2dc-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="2f2dc-115">Cell name:</span></span>  <br/> |<span data-ttu-id="2f2dc-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="2f2dc-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="2f2dc-117">プログラムからインデックスによって [NoProofing] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f2dc-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f2dc-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f2dc-118">Section index:</span></span>  <br/> |<span data-ttu-id="2f2dc-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2f2dc-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2f2dc-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f2dc-120">Row index:</span></span>  <br/> |<span data-ttu-id="2f2dc-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2f2dc-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="2f2dc-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2f2dc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2f2dc-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="2f2dc-123">**visObjNoProofing**</span></span> <br/> |
   

