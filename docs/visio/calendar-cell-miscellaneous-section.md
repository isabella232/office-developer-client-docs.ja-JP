---
title: '[Calendar] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: セル数式が Date 情報を含むときに使用するカレンダーを指定します。
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421817"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="5eca7-103">[Calendar] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="5eca7-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5eca7-104">セル数式が Date 情報を含むときに使用するカレンダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="5eca7-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5eca7-105">注釈</span><span class="sxs-lookup"><span data-stu-id="5eca7-105">Remarks</span></span>

<span data-ttu-id="5eca7-106">使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。</span><span class="sxs-lookup"><span data-stu-id="5eca7-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="5eca7-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5eca7-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eca7-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="5eca7-108">Cell name:</span></span>  <br/> | <span data-ttu-id="5eca7-109">カレンダー</span><span class="sxs-lookup"><span data-stu-id="5eca7-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="5eca7-110">プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5eca7-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eca7-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eca7-111">Section index:</span></span>  <br/> |<span data-ttu-id="5eca7-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5eca7-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5eca7-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eca7-113">Row index:</span></span>  <br/> |<span data-ttu-id="5eca7-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5eca7-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5eca7-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eca7-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5eca7-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="5eca7-116">**visObjCalendar**</span></span> <br/> |
   

