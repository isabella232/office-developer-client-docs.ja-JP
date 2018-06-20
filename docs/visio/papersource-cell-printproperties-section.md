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
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805970"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="3b83b-103">[PaperSource] セル ([PrintProperties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3b83b-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="3b83b-104">用紙の給紙方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b83b-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b83b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3b83b-105">Remarks</span></span>

<span data-ttu-id="3b83b-106">この設定設定に対応して、**給紙方法****プリンターの設定**] ダイアログ ボックス ([**デザイン**] タブで、**ページ設定**の矢印をクリックし、[**印刷設定**] タブで、[**設定**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="3b83b-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="3b83b-107">箱選択範囲の場合、Microsoft Windows wingdi.h ファイルで定義されているこのセルにマップ (DMBIN で始まる) の定数に含まれる数値たとえば、7 の値は、DMBIN_AUTO を表します。</span><span class="sxs-lookup"><span data-stu-id="3b83b-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="3b83b-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって PaperSource] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b83b-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b83b-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="3b83b-109">Cell name:</span></span>  <br/> |<span data-ttu-id="3b83b-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="3b83b-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="3b83b-111">プログラムから、インデックスによって [PaperSource] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b83b-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b83b-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b83b-112">Section index:</span></span>  <br/> |<span data-ttu-id="3b83b-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b83b-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3b83b-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b83b-114">Row index:</span></span>  <br/> |<span data-ttu-id="3b83b-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="3b83b-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="3b83b-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b83b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="3b83b-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="3b83b-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

