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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799989"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="d2f38-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="d2f38-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="d2f38-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2f38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2f38-105">オプション ボタン グループの一部となる 1 つのラジオ ・ ボタンをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2f38-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="d2f38-106">ラジオ ボタン グループは、表示された表から組み込まれているダイアログ ボックスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d2f38-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2f38-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d2f38-107">Header file:</span></span>  <br/> |<span data-ttu-id="d2f38-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2f38-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d2f38-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="d2f38-109">Members</span></span>

 <span data-ttu-id="d2f38-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="d2f38-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="d2f38-111">ラジオ ・ ボタンの文字の文字列のラベルのメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="d2f38-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="d2f38-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d2f38-112">**ulFlags**</span></span>
  
> <span data-ttu-id="d2f38-113">**UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d2f38-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="d2f38-114">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d2f38-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="d2f38-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2f38-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d2f38-116">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="d2f38-116">The label is in Unicode format.</span></span> <span data-ttu-id="d2f38-117">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="d2f38-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="d2f38-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="d2f38-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="d2f38-119">ラジオ ボタン グループ内のボタンの数。</span><span class="sxs-lookup"><span data-stu-id="d2f38-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="d2f38-120">表示された表の一連の行では、グループ内の他のボタンの**DTBLRADIOBUTTON**構造体を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f38-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="d2f38-121">**UlcButtons**メンバーのそれぞれの行、同じ値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f38-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="d2f38-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d2f38-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="d2f38-123">型 PT_LONG のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d2f38-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="d2f38-124">ラジオ ボタン グループの最初の選択は、このプロパティの初期値に基づきます。</span><span class="sxs-lookup"><span data-stu-id="d2f38-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="d2f38-125">グループ内の各ボタンには、 **ulPropTag**の同じプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f38-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="d2f38-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="d2f38-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="d2f38-127">選択したボタンを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="d2f38-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2f38-128">備考</span><span class="sxs-lookup"><span data-stu-id="d2f38-128">Remarks</span></span>

<span data-ttu-id="d2f38-129">**DTBLRADIOBUTTON**構造体では、ラジオ ボタンのボタンのグループに関連付けられているボタン コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2f38-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="d2f38-130">グループ内のボタンを 1 つだけをチェックすることができます。設定するグループの他のボタンを 1 つのボタンを設定します。</span><span class="sxs-lookup"><span data-stu-id="d2f38-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="d2f38-131">ボタンの数は、グループ内のラジオ ボタンの数です。</span><span class="sxs-lookup"><span data-stu-id="d2f38-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="d2f38-132">グループ内の他のオプション ボタンの構造体は、表示された表のそれ以降の行でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d2f38-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="d2f38-133">各構造体は、そのボタンの数の値が同じで必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2f38-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="d2f38-134">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f38-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="d2f38-135">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2f38-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2f38-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2f38-136">See also</span></span>



[<span data-ttu-id="d2f38-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d2f38-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="d2f38-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="d2f38-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="d2f38-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="d2f38-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="d2f38-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d2f38-140">MAPI Structures</span></span>](mapi-structures.md)

