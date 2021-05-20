---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436833"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="2b50a-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="2b50a-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="2b50a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b50a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b50a-105">表示テーブルから作成されたダイアログ ボックスで使用されるチェック ボックスに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2b50a-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b50a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2b50a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b50a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b50a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b50a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2b50a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="2b50a-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="2b50a-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="2b50a-110">Members</span><span class="sxs-lookup"><span data-stu-id="2b50a-110">Members</span></span>

 <span data-ttu-id="2b50a-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="2b50a-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="2b50a-112">チェック ボックスと一緒に表示される文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="2b50a-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="2b50a-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2b50a-113">**ulFlags**</span></span>
  
> <span data-ttu-id="2b50a-114">チェック ボックス ラベルの形式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2b50a-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="2b50a-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-115">The following flag can be set:</span></span>
    
<span data-ttu-id="2b50a-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b50a-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2b50a-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2b50a-117">The label is in Unicode format.</span></span> <span data-ttu-id="2b50a-118">このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2b50a-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="2b50a-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="2b50a-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="2b50a-120">型のプロパティのプロパティ タグPT_BOOLEAN。</span><span class="sxs-lookup"><span data-stu-id="2b50a-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="2b50a-121">このプロパティの値は、チェック ボックスの状態の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b50a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="2b50a-122">Remarks</span></span>

<span data-ttu-id="2b50a-123">**DTBLCHECKBOX** 構造体は、有効 (チェック ボックス) または無効 (空のボックス) の 2 つの状態のいずれかを反映するコントロールのチェック ボックスを表します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="2b50a-124">**ulPRPropertyName** メンバーは、チェック ボックスの状態を変更することによって値が操作されるブール型 (Boolean) のプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="2b50a-125">チェック ボックスが最初に表示される場合、MAPI は、表示テーブルに関連付けられている **IMAPIProp** 実装の **GetProps** メソッドを呼び出して、一連の既定のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="2b50a-126">プロパティの 1 つが **DTBLCHECKBOX** 構造体のプロパティ タグにマップされている場合、そのプロパティの値がチェック ボックスの初期値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="2b50a-127">チェック ボックス コントロールは変更可能です。</span><span class="sxs-lookup"><span data-stu-id="2b50a-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="2b50a-128">これにより、ユーザーは状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-128">This allows a user to change their states.</span></span> <span data-ttu-id="2b50a-129">変更可能なチェック ボックスは [、DTCTL](dtctl.md)構造の **ulCtlFlags** メンバーおよび PR_CONTROL_FLAGS ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに **DT_EDITABLE** フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="2b50a-130">チェック ボックスの状態が変更されると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して **、DTBLCHECKBOX** 構造体のプロパティ タグ メンバーで識別されるプロパティを新しい状態に設定します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="2b50a-131">**たとえば、アドレス** 帳プロバイダーの構成ダイアログ ボックスに変更可能なチェック ボックス コントロールを含め、受信者の PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティの設定を調整できます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="2b50a-132">ユーザーがチェック ボックスをオンにすると、MAPI は、このプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2b50a-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="2b50a-133">チェック ボックスがオフの場合、プロパティは FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2b50a-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="2b50a-134">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="2b50a-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2b50a-135">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="2b50a-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="2b50a-136">プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="2b50a-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b50a-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b50a-137">See also</span></span>



[<span data-ttu-id="2b50a-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2b50a-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="2b50a-139">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b50a-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="2b50a-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2b50a-140">MAPI Structures</span></span>](mapi-structures.md)

