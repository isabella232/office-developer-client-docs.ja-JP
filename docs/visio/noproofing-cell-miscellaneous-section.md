---
title: '[noproofing] セル ([その他] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペルを自動的に修正するかどうか、および選択した図形のスペルミスを表示するかどうかを指定します。 ブール値を受け取ります。
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357226"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="89684-104">[noproofing] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="89684-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="89684-105">スペルを自動的に修正するかどうか、および選択した図形のスペルミスを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="89684-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="89684-106">**ブール**値を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="89684-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="89684-107">**値**</span><span class="sxs-lookup"><span data-stu-id="89684-107">**Value**</span></span>|<span data-ttu-id="89684-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="89684-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89684-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="89684-109">TRUE</span></span>  <br/> |<span data-ttu-id="89684-110">スペルチェックは自動的には修正されず、選択した図形のスペルミスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="89684-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="89684-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="89684-111">FALSE</span></span>  <br/> |<span data-ttu-id="89684-112">スペルチェックは自動的に修正され、選択した図形のスペルミスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89684-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89684-113">解説</span><span class="sxs-lookup"><span data-stu-id="89684-113">Remarks</span></span>

<span data-ttu-id="89684-114">別の数式または**CellsU**プロパティを使用してプログラムから、名前によって [noproofing] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="89684-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89684-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="89684-115">Cell name:</span></span>  <br/> |<span data-ttu-id="89684-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="89684-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="89684-117">プログラムから、インデックスによって [noproofing] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="89684-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89684-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="89684-118">Section index:</span></span>  <br/> |<span data-ttu-id="89684-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="89684-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="89684-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="89684-120">Row index:</span></span>  <br/> |<span data-ttu-id="89684-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="89684-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="89684-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="89684-122">Cell index:</span></span>  <br/> |<span data-ttu-id="89684-123">**visobjnoproofing**</span><span class="sxs-lookup"><span data-stu-id="89684-123">**visObjNoProofing**</span></span> <br/> |
   

