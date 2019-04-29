---
title: '[Tip] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを置いたときに表示されます。セルではヒントの文字列は自動的に引用符で囲まれますが、ツール ヒントには引用符は表示されません。
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424862"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="9bc92-104">[Tip] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="9bc92-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="9bc92-p102">ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを置いたときに表示されます。セルではヒントの文字列は自動的に引用符で囲まれますが、ツール ヒントには引用符は表示されません。</span><span class="sxs-lookup"><span data-stu-id="9bc92-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9bc92-107">注釈</span><span class="sxs-lookup"><span data-stu-id="9bc92-107">Remarks</span></span>

<span data-ttu-id="9bc92-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Tip] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9bc92-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9bc92-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9bc92-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9bc92-110">管理.</span><span class="sxs-lookup"><span data-stu-id="9bc92-110">Controls.</span></span>  <span data-ttu-id="9bc92-111">*名前*です。ヒントコントロールの場所。</span><span class="sxs-lookup"><span data-stu-id="9bc92-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="9bc92-112">*name*は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="9bc92-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="9bc92-113">プログラムから、インデックスによって [Tip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9bc92-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9bc92-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9bc92-114">Section index:</span></span>  <br/> |<span data-ttu-id="9bc92-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="9bc92-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="9bc92-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9bc92-116">Row index:</span></span>  <br/> |<span data-ttu-id="9bc92-117">**visRowControl** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="9bc92-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9bc92-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9bc92-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9bc92-119">**visctltip**</span><span class="sxs-lookup"><span data-stu-id="9bc92-119">**visCtlTip**</span></span> <br/> |
   

