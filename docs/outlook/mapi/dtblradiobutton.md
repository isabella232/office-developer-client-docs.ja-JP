---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569744"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="05c92-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="05c92-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="05c92-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05c92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05c92-105">オプション ボタン グループの一部となる 1 つのラジオ ・ ボタンをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="05c92-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="05c92-106">ラジオ ボタン グループは、表示された表から組み込まれているダイアログ ボックスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="05c92-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05c92-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="05c92-107">Header file:</span></span>  <br/> |<span data-ttu-id="05c92-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05c92-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="05c92-109">Members</span><span class="sxs-lookup"><span data-stu-id="05c92-109">Members</span></span>

 <span data-ttu-id="05c92-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="05c92-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="05c92-111">ラジオ ・ ボタンの文字の文字列のラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="05c92-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="05c92-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="05c92-112">**ulFlags**</span></span>
  
> <span data-ttu-id="05c92-113">**UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="05c92-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="05c92-114">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="05c92-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="05c92-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05c92-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="05c92-116">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="05c92-116">The label is in Unicode format.</span></span> <span data-ttu-id="05c92-117">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="05c92-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="05c92-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="05c92-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="05c92-119">ラジオ ボタン グループ内のボタンの数。</span><span class="sxs-lookup"><span data-stu-id="05c92-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="05c92-120">表示された表の一連の行では、グループ内の他のボタンの**DTBLRADIOBUTTON**構造体を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="05c92-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="05c92-121">**UlcButtons**メンバーのそれぞれの行、同じ値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="05c92-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="05c92-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="05c92-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="05c92-123">型 PT_LONG のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="05c92-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="05c92-124">ラジオ ボタン グループの最初の選択は、このプロパティの初期値に基づきます。</span><span class="sxs-lookup"><span data-stu-id="05c92-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="05c92-125">グループ内の各ボタンには、 **ulPropTag**の同じプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05c92-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="05c92-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="05c92-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="05c92-127">選択したボタンを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="05c92-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05c92-128">注釈</span><span class="sxs-lookup"><span data-stu-id="05c92-128">Remarks</span></span>

<span data-ttu-id="05c92-129">**DTBLRADIOBUTTON**構造体では、ラジオ ボタンのボタンのグループに関連付けられているボタン コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="05c92-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="05c92-130">グループ内のボタンを 1 つだけをチェックすることができます。設定するグループの他のボタンを 1 つのボタンを設定します。</span><span class="sxs-lookup"><span data-stu-id="05c92-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="05c92-131">ボタンの数は、グループ内のラジオ ボタンの数です。</span><span class="sxs-lookup"><span data-stu-id="05c92-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="05c92-132">グループ内の他のオプション ボタンの構造体は、表示された表のそれ以降の行でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="05c92-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="05c92-133">各構造体は、そのボタンの数の値が同じで必要があります。</span><span class="sxs-lookup"><span data-stu-id="05c92-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="05c92-134">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05c92-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="05c92-135">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05c92-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05c92-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="05c92-136">See also</span></span>



[<span data-ttu-id="05c92-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="05c92-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="05c92-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="05c92-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="05c92-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="05c92-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="05c92-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="05c92-140">MAPI Structures</span></span>](mapi-structures.md)

