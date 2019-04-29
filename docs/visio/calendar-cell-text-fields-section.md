---
title: '[Calendar] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424755"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="7475d-103">[Calendar] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="7475d-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="7475d-104">データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="7475d-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7475d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="7475d-105">Remarks</span></span>

<span data-ttu-id="7475d-106">使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。</span><span class="sxs-lookup"><span data-stu-id="7475d-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="7475d-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7475d-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7475d-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7475d-108">Cell name:</span></span>  <br/> | <span data-ttu-id="7475d-109">フィールド。 *i* = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="7475d-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7475d-110">プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7475d-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7475d-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7475d-111">Section index:</span></span>  <br/> |<span data-ttu-id="7475d-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="7475d-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="7475d-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7475d-113">Row index:</span></span>  <br/> |<span data-ttu-id="7475d-114">**visRowField** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="7475d-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7475d-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7475d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="7475d-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="7475d-116">**visFieldCalendar**</span></span> <br/> |
   

