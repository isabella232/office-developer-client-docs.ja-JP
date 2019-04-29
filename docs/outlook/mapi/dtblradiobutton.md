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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434600"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="2f81f-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="2f81f-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="2f81f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f81f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f81f-105">ラジオボタングループの一部となる1つのラジオボタンを表します。</span><span class="sxs-lookup"><span data-stu-id="2f81f-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="2f81f-106">ラジオボタングループは、表示テーブルから構築されたダイアログボックスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f81f-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f81f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2f81f-107">Header file:</span></span>  <br/> |<span data-ttu-id="2f81f-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f81f-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="2f81f-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="2f81f-109">Members</span></span>

 <span data-ttu-id="2f81f-110">**ulblpszlabel**</span><span class="sxs-lookup"><span data-stu-id="2f81f-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2f81f-111">ラジオボタンの文字列ラベルの文字をメモリ内に配置します。</span><span class="sxs-lookup"><span data-stu-id="2f81f-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="2f81f-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2f81f-112">**ulFlags**</span></span>
  
> <span data-ttu-id="2f81f-113">**ulblpszlabel**メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2f81f-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="2f81f-114">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f81f-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="2f81f-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2f81f-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2f81f-116">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2f81f-116">The label is in Unicode format.</span></span> <span data-ttu-id="2f81f-117">MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="2f81f-118">**ulcbuttons**</span><span class="sxs-lookup"><span data-stu-id="2f81f-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="2f81f-119">ラジオボタングループのボタン数。</span><span class="sxs-lookup"><span data-stu-id="2f81f-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="2f81f-120">グループ内の他のボタンの**dtblradiobutton**構造体は、表示テーブルの連続する行に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="2f81f-121">これらの各行には、 **ulcbuttons**メンバーと同じ値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="2f81f-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="2f81f-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="2f81f-123">PT_LONG 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="2f81f-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="2f81f-124">ラジオボタングループでの最初の選択は、このプロパティの初期値に基づいています。</span><span class="sxs-lookup"><span data-stu-id="2f81f-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="2f81f-125">グループ内の各ボタンには、 **ulPropTag**を同じプロパティに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="2f81f-126">**lreturnvalue**</span><span class="sxs-lookup"><span data-stu-id="2f81f-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="2f81f-127">選択したボタンを識別する一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="2f81f-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f81f-128">注釈</span><span class="sxs-lookup"><span data-stu-id="2f81f-128">Remarks</span></span>

<span data-ttu-id="2f81f-129">**dtblradiobutton**構造体は、ボタンのグループに関連付けられているボタンコントロールのラジオボタンを表します。</span><span class="sxs-lookup"><span data-stu-id="2f81f-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="2f81f-130">グループ内の1つのボタンだけをチェックできます。1つのボタンを設定すると、グループ内の他のボタンが未設定になります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="2f81f-131">[ボタン数] は、グループ内のオプションボタンの数を示します。</span><span class="sxs-lookup"><span data-stu-id="2f81f-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="2f81f-132">グループ内の他のオプションボタンの構造は、表示テーブル内の後続の行にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="2f81f-133">これらの各構造体は、ボタンの数と同じ値を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f81f-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="2f81f-134">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f81f-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2f81f-135">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f81f-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f81f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f81f-136">See also</span></span>



[<span data-ttu-id="2f81f-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="2f81f-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="2f81f-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2f81f-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="2f81f-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="2f81f-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="2f81f-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2f81f-140">MAPI Structures</span></span>](mapi-structures.md)

