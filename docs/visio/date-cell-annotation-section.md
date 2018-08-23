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
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805181"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="71414-103">[Date] セル ([注釈] セクション)</span><span class="sxs-lookup"><span data-stu-id="71414-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="71414-104">コメントを最後に編集した日付と時刻が含まれます。</span><span class="sxs-lookup"><span data-stu-id="71414-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71414-105">このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="71414-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="71414-106">Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="71414-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="71414-107">備考</span><span class="sxs-lookup"><span data-stu-id="71414-107">Remarks</span></span>

<span data-ttu-id="71414-108">ユーザー インターフェイスのコメント ボックスには、日付のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="71414-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="71414-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Date] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="71414-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71414-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="71414-110">Cell name:</span></span>  <br/> | <span data-ttu-id="71414-111">Annotation.Date [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="71414-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="71414-112">プログラムから、インデックスによって [Date] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="71414-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71414-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="71414-113">Section index:</span></span>  <br/> |<span data-ttu-id="71414-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="71414-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="71414-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="71414-115">Row index:</span></span>  <br/> |<span data-ttu-id="71414-116">**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="71414-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="71414-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="71414-117">Cell index:</span></span>  <br/> |<span data-ttu-id="71414-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="71414-118">**visAnnotationDate**</span></span> <br/> |
   

