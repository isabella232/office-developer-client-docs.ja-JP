---
title: '[PaperSource] セル ([PrintProperties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: 用紙の給紙方法を指定します。
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301464"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="60f8f-103">[PaperSource] セル ([PrintProperties] セクション)</span><span class="sxs-lookup"><span data-stu-id="60f8f-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="60f8f-104">用紙の給紙方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="60f8f-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60f8f-105">解説</span><span class="sxs-lookup"><span data-stu-id="60f8f-105">Remarks</span></span>

<span data-ttu-id="60f8f-106">この設定は、[**プリンターの設定**] ダイアログ ボックスの [**給紙**] の設定に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**プリンターの設定**] タブで [**設定**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="60f8f-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="60f8f-107">このセルの数値は、Microsoft Windows ウィング di .h ファイルの bin 選択に対して定義されている定数 (dmbin で始まります) に対応しています。たとえば、値7は DMBIN_AUTO を表します。</span><span class="sxs-lookup"><span data-stu-id="60f8f-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="60f8f-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [pagesource] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="60f8f-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60f8f-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="60f8f-109">Cell name:</span></span>  <br/> |<span data-ttu-id="60f8f-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="60f8f-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="60f8f-111">プログラムから、インデックスによって [pagesource] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="60f8f-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60f8f-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="60f8f-112">Section index:</span></span>  <br/> |<span data-ttu-id="60f8f-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60f8f-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="60f8f-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="60f8f-114">Row index:</span></span>  <br/> |<span data-ttu-id="60f8f-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="60f8f-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="60f8f-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="60f8f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="60f8f-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="60f8f-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

