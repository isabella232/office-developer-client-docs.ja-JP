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
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408447"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="61219-103">[PaperKind] セル ([Print Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="61219-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="61219-104">ページを印刷する用紙の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="61219-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61219-105">注釈</span><span class="sxs-lookup"><span data-stu-id="61219-105">Remarks</span></span>

<span data-ttu-id="61219-106">この設定は、[印刷設定] ダイアログ ボックスの [用紙サイズ]設定に対応します([デザイン] タブの[ページ設定] 矢印をクリックし、[印刷セットアップ] タブで [セットアップ] ボタンを **クリック** します)。</span><span class="sxs-lookup"><span data-stu-id="61219-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="61219-107">このセル内の数値は、Microsoft Windows wingdi.h ファイルの用紙選択に対して定義された定数 (DMPAPER のプレフィックス) にマップされます。</span><span class="sxs-lookup"><span data-stu-id="61219-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="61219-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageKind] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="61219-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61219-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="61219-109">Cell name:</span></span>  <br/> |<span data-ttu-id="61219-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="61219-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="61219-111">プログラムから、インデックスによって [PaperKind] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="61219-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61219-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="61219-112">Section index:</span></span>  <br/> |<span data-ttu-id="61219-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61219-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="61219-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="61219-114">Row index:</span></span>  <br/> |<span data-ttu-id="61219-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="61219-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="61219-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="61219-116">Cell index:</span></span>  <br/> |<span data-ttu-id="61219-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="61219-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

