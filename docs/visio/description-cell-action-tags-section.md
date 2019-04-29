---
title: '[Description] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415762"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="0a834-103">[Description] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="0a834-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="0a834-104">アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a834-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a834-105">注釈</span><span class="sxs-lookup"><span data-stu-id="0a834-105">Remarks</span></span>

<span data-ttu-id="0a834-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0a834-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a834-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="0a834-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0a834-108">タグ.</span><span class="sxs-lookup"><span data-stu-id="0a834-108">SmartTags.</span></span>  <span data-ttu-id="0a834-109">*名前*です。SmartTags の説明。</span><span class="sxs-lookup"><span data-stu-id="0a834-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="0a834-110">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="0a834-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0a834-111">プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a834-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a834-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a834-112">Section index:</span></span>  <br/> |<span data-ttu-id="0a834-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0a834-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0a834-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a834-114">Row index:</span></span>  <br/> |<span data-ttu-id="0a834-115">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="0a834-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0a834-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0a834-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0a834-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="0a834-117">**visSmartTagDescription**</span></span> <br/> |
   

