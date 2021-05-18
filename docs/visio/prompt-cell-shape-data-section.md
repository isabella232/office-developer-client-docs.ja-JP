---
title: '[Prompt] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: '[図形データ] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。'
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405486"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="a4de5-103">[Prompt] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="a4de5-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="a4de5-104">[**図形データ**] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a4de5-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a4de5-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a4de5-105">Remarks</span></span>

<span data-ttu-id="a4de5-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Prompt] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a4de5-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4de5-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a4de5-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a4de5-108">Prop。  *Name*  .[名前]  *が行*  名のプロンプト</span><span class="sxs-lookup"><span data-stu-id="a4de5-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a4de5-109">プログラムから、インデックスによって [Prompt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4de5-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4de5-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4de5-110">Section index:</span></span>  <br/> |<span data-ttu-id="a4de5-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="a4de5-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="a4de5-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4de5-112">Row index:</span></span>  <br/> |<span data-ttu-id="a4de5-113">**visRowProp +** *i*  *=*  0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a4de5-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a4de5-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a4de5-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a4de5-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="a4de5-115">**visCustPropsPrompt**</span></span> <br/> |
   

