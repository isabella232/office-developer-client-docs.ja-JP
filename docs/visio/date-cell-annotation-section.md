---
title: '[Date] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: コメントを最後に編集した日付と時刻が含まれます。
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423882"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="86e67-103">[Date] セル ([Annotation] セクション)</span><span class="sxs-lookup"><span data-stu-id="86e67-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="86e67-104">コメントを最後に編集した日付と時刻が含まれます。</span><span class="sxs-lookup"><span data-stu-id="86e67-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="86e67-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="86e67-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="86e67-106">これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="86e67-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86e67-107">注釈</span><span class="sxs-lookup"><span data-stu-id="86e67-107">Remarks</span></span>

<span data-ttu-id="86e67-108">ユーザー インターフェイスのコメント ボックスには、日付のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="86e67-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="86e67-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Date] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="86e67-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86e67-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="86e67-110">Cell name:</span></span>  <br/> | <span data-ttu-id="86e67-111">注釈. Date [ *i* ] = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="86e67-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="86e67-112">プログラムから、インデックスによって [Date] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="86e67-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86e67-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="86e67-113">Section index:</span></span>  <br/> |<span data-ttu-id="86e67-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="86e67-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="86e67-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="86e67-115">Row index:</span></span>  <br/> |<span data-ttu-id="86e67-116">**visRowAnnotation** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="86e67-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="86e67-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="86e67-117">Cell index:</span></span>  <br/> |<span data-ttu-id="86e67-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="86e67-118">**visAnnotationDate**</span></span> <br/> |
   

