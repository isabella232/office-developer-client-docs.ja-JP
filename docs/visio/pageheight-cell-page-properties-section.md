---
title: '[PageHeight] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: 図面単位で表した印刷ページの高さを指定します。
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334350"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="37c22-103">[PageHeight] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="37c22-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="37c22-104">図面単位で表した印刷ページの高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="37c22-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37c22-105">解説</span><span class="sxs-lookup"><span data-stu-id="37c22-105">Remarks</span></span>

<span data-ttu-id="37c22-106">ページの高さは、[**ページ設定**] ダイアログ ボックス ([**デザイン**] タブで [**ページ設定**] 矢印をクリック) の [**ページ サイズ**] タブで設定することも、マウスを使用してページのサイズを手動で変更して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="37c22-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="37c22-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageHeight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="37c22-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37c22-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="37c22-108">Cell name:</span></span>  <br/> |<span data-ttu-id="37c22-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="37c22-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="37c22-110">プログラムから、インデックスによる [PageHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="37c22-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37c22-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37c22-111">Section index:</span></span>  <br/> |<span data-ttu-id="37c22-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37c22-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37c22-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37c22-113">Row index:</span></span>  <br/> |<span data-ttu-id="37c22-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="37c22-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="37c22-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37c22-115">Cell index:</span></span>  <br/> |<span data-ttu-id="37c22-116">**vispageheight**</span><span class="sxs-lookup"><span data-stu-id="37c22-116">**visPageHeight**</span></span> <br/> |
   

