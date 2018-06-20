---
title: '[PaperKind] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: ページを印刷する用紙の種類を指定します。
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805974"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="77eca-103">[PaperKind] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="77eca-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="77eca-104">ページを印刷する用紙の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="77eca-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77eca-105">注釈</span><span class="sxs-lookup"><span data-stu-id="77eca-105">Remarks</span></span>

<span data-ttu-id="77eca-106">この設定は、[**印刷設定**] ダイアログ ボックスで**用紙サイズ**の設定に対応して ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックし、[**プリンターの設定**] タブで、**設定**ボタンをクリック) します。</span><span class="sxs-lookup"><span data-stu-id="77eca-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="77eca-107">用紙の Microsoft Windows wingdi.h ファイル内のこのセルにマップが付いて DMPAPER) の定数に含まれる数値が定義されています。</span><span class="sxs-lookup"><span data-stu-id="77eca-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="77eca-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PaperKind] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="77eca-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77eca-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="77eca-109">Cell name:</span></span>  <br/> |<span data-ttu-id="77eca-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="77eca-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="77eca-111">プログラムから、インデックスによって [PaperKind] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="77eca-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77eca-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="77eca-112">Section index:</span></span>  <br/> |<span data-ttu-id="77eca-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="77eca-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="77eca-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="77eca-114">Row index:</span></span>  <br/> |<span data-ttu-id="77eca-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="77eca-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="77eca-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="77eca-116">Cell index:</span></span>  <br/> |<span data-ttu-id="77eca-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="77eca-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

