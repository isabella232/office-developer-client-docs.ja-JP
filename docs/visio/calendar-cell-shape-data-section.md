---
title: '[Calendar] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: データ型が Date の場合に図形データに使用される予定表を指定します。
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432759"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="8315b-103">[Calendar] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="8315b-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="8315b-104">データ型が Date の場合に図形データに使用される予定表を指定します。</span><span class="sxs-lookup"><span data-stu-id="8315b-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8315b-105">注釈</span><span class="sxs-lookup"><span data-stu-id="8315b-105">Remarks</span></span>

<span data-ttu-id="8315b-106">使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。</span><span class="sxs-lookup"><span data-stu-id="8315b-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="8315b-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8315b-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8315b-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="8315b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8315b-109">Prop。  *name*  .Prop のカレンダー。  *name*  は行名です</span><span class="sxs-lookup"><span data-stu-id="8315b-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8315b-110">プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8315b-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8315b-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8315b-111">Section index:</span></span>  <br/> |<span data-ttu-id="8315b-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="8315b-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="8315b-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8315b-113">Row index:</span></span>  <br/> |<span data-ttu-id="8315b-114">**visRowProp**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8315b-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8315b-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8315b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8315b-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="8315b-116">**visCustPropsCalendar**</span></span> <br/> |
   

