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
description: データ型が Date のとき図形データに使用するカレンダーを指定します。
ms.openlocfilehash: 502ecd8a028c4c0d9841bbd3e0ed369f73bd6b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804945"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="62bf0-103">[Calendar] セル ([図形データ] セクション)</span><span class="sxs-lookup"><span data-stu-id="62bf0-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="62bf0-104">データ型が Date のとき図形データに使用するカレンダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="62bf0-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62bf0-105">備考</span><span class="sxs-lookup"><span data-stu-id="62bf0-105">Remarks</span></span>

<span data-ttu-id="62bf0-106">使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。</span><span class="sxs-lookup"><span data-stu-id="62bf0-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="62bf0-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="62bf0-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62bf0-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="62bf0-108">Cell name:</span></span>  <br/> | <span data-ttu-id="62bf0-109">プロペラです。 *名*です。予定表、プロペラします。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="62bf0-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="62bf0-110">プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62bf0-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62bf0-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bf0-111">Section index:</span></span>  <br/> |<span data-ttu-id="62bf0-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="62bf0-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="62bf0-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bf0-113">Row index:</span></span>  <br/> |<span data-ttu-id="62bf0-114">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="62bf0-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="62bf0-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="62bf0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="62bf0-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="62bf0-116">**visCustPropsCalendar**</span></span> <br/> |
   

