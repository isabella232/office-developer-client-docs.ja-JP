---
title: '[UIVisibility] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357219"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="2de01-103">[UIVisibility] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="2de01-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="2de01-104">ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2de01-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="2de01-105">**値**</span><span class="sxs-lookup"><span data-stu-id="2de01-105">**Value**</span></span>|<span data-ttu-id="2de01-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="2de01-106">**Description**</span></span>|<span data-ttu-id="2de01-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="2de01-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2de01-108">.0</span><span class="sxs-lookup"><span data-stu-id="2de01-108">0</span></span>  <br/> |<span data-ttu-id="2de01-109">UI 内にページ名を表示します (既定値)。</span><span class="sxs-lookup"><span data-stu-id="2de01-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="2de01-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="2de01-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="2de01-111">1-d</span><span class="sxs-lookup"><span data-stu-id="2de01-111">1</span></span>  <br/> |<span data-ttu-id="2de01-112">UI 内にページ名を表示しません。</span><span class="sxs-lookup"><span data-stu-id="2de01-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="2de01-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="2de01-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2de01-114">解説</span><span class="sxs-lookup"><span data-stu-id="2de01-114">Remarks</span></span>

<span data-ttu-id="2de01-115">[UIVisibility] セルを **visUIVHidden** に設定すると、ページ名を含む文字列を表示する UI のどの部分にも、ページが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2de01-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="2de01-116">たとえば、[**ドローイング エクスプローラー**] 内、または [ページ] タブ上で、ページがオプションとして表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2de01-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="2de01-117">ただし、ページ名を含まないオートメーションまたは UI パス (たとえば、[**印刷**] コマンド) を使用する場合は、ページにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2de01-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="2de01-118">このセルは、図面ページ専用であり、校正履歴のオーバレイ ページ用ではありません。既定では [UIVisibility] セルが **visUIVHidden** に設定されますが、この値を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="2de01-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2de01-119">ページをドキュメントの**印刷**コマンドから非表示にするには、背景ページ (**Type**プロパティは**visTypeBackground** ) を使用して、どのページでも使用されていない (背景ページ上の図形を背景として使用するページで印刷する)印刷されます)。</span><span class="sxs-lookup"><span data-stu-id="2de01-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="2de01-120">ドキュメントの [**印刷**] コマンドはインデックスが作成されたページでのみ動作し、背景ページにインデックスは作成されません。</span><span class="sxs-lookup"><span data-stu-id="2de01-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="2de01-121">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UIVisibility] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2de01-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2de01-122">セル名 :</span><span class="sxs-lookup"><span data-stu-id="2de01-122">Cell name:</span></span>  <br/> |<span data-ttu-id="2de01-123">[uivisibility]</span><span class="sxs-lookup"><span data-stu-id="2de01-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="2de01-124">プログラムから、インデックスによって [UIVisibility] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2de01-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2de01-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2de01-125">Section index:</span></span>  <br/> |<span data-ttu-id="2de01-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2de01-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2de01-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2de01-127">Row index:</span></span>  <br/> |<span data-ttu-id="2de01-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="2de01-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="2de01-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2de01-129">Cell index:</span></span>  <br/> |<span data-ttu-id="2de01-130">**vispageuivisibility**</span><span class="sxs-lookup"><span data-stu-id="2de01-130">**visPageUIVisibility**</span></span> <br/> |
   

