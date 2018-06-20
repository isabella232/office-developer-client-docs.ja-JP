---
title: '[ViewMarkup] セル ([Document Properties] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: 図面ウィンドウに校正履歴を表示するかどうかを指定します。
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806780"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="3e37a-103">[ViewMarkup] セル ([Document Properties] セクション</span><span class="sxs-lookup"><span data-stu-id="3e37a-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="3e37a-104">図面ウィンドウに校正履歴を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3e37a-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="3e37a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3e37a-105">**Value**</span></span>|<span data-ttu-id="3e37a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3e37a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e37a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e37a-107">TRUE</span></span>  <br/> |<span data-ttu-id="3e37a-108">図面ウィンドウに校正履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="3e37a-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="3e37a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e37a-109">FALSE</span></span>  <br/> |<span data-ttu-id="3e37a-110">校正履歴を表示しません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="3e37a-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e37a-111">注釈</span><span class="sxs-lookup"><span data-stu-id="3e37a-111">Remarks</span></span>

 <span data-ttu-id="3e37a-112">校正履歴の記録を有効にすると ([addmarkup] セルが TRUE)、ViewMarkup セルが自動的に TRUE に設定し、校正履歴の記録がオフになっている後でも TRUE のまま ([addmarkup] セルでは FALSE です)。</span><span class="sxs-lookup"><span data-stu-id="3e37a-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="3e37a-113">AddMarkup セルが TRUE の場合に、[ViewMarkup] セルの値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="3e37a-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="3e37a-114">図面にコメントを挿入した場合、校正履歴の記録機能がオンかどうかに関わらず、[ViewMarkup] セルは TRUE に設定されます。[ViewMarkup] セルが TRUE でなければ、図面内にコメントが表示されません。</span><span class="sxs-lookup"><span data-stu-id="3e37a-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="3e37a-115">このセルは、[**校閲**] タブには、**マークアップ**のグループ内の**コメントの表示**コマンドに対応します。</span><span class="sxs-lookup"><span data-stu-id="3e37a-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="3e37a-116">取得する、[ViewMarkup] セルへの参照名を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e37a-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e37a-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3e37a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="3e37a-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="3e37a-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="3e37a-119">プログラムから、インデックスによって [ViewMarkup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e37a-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e37a-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e37a-120">Section index:</span></span>  <br/> |<span data-ttu-id="3e37a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e37a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3e37a-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e37a-122">Row index:</span></span>  <br/> |<span data-ttu-id="3e37a-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="3e37a-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="3e37a-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3e37a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="3e37a-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="3e37a-125">**visDocViewMarkup**</span></span> <br/> |
   

