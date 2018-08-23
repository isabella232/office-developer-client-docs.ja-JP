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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799964"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="98ca9-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="98ca9-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="98ca9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98ca9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98ca9-105">ダイアログ ボックスが表示テーブルの構築に使用するチェック ボックスに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98ca9-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98ca9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="98ca9-106">Header file:</span></span>  <br/> |<span data-ttu-id="98ca9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98ca9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="98ca9-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="98ca9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="98ca9-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="98ca9-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="98ca9-110">Members</span><span class="sxs-lookup"><span data-stu-id="98ca9-110">Members</span></span>

 <span data-ttu-id="98ca9-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="98ca9-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="98ca9-112">チェック ボックスが表示されている文字の文字列のメモリ内の位置。</span><span class="sxs-lookup"><span data-stu-id="98ca9-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="98ca9-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="98ca9-113">**ulFlags**</span></span>
  
> <span data-ttu-id="98ca9-114">チェック ボックスのラベルの書式を指定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="98ca9-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="98ca9-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="98ca9-115">The following flag can be set:</span></span>
    
<span data-ttu-id="98ca9-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98ca9-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="98ca9-117">ラベルは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="98ca9-117">The label is in Unicode format.</span></span> <span data-ttu-id="98ca9-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。</span><span class="sxs-lookup"><span data-stu-id="98ca9-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="98ca9-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="98ca9-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="98ca9-120">型 PT_BOOLEAN のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="98ca9-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="98ca9-121">このプロパティの値は、チェック ボックスの状態の影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="98ca9-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98ca9-122">注釈</span><span class="sxs-lookup"><span data-stu-id="98ca9-122">Remarks</span></span>

<span data-ttu-id="98ca9-123">**DTBLCHECKBOX**構造体が 2 つの状態を反映するコントロールのチェック ボックスを示します: (チェック ボックス) を有効になっているか、(空のボックス) を無効にします。</span><span class="sxs-lookup"><span data-stu-id="98ca9-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="98ca9-124">**UlPRPropertyName**メンバーは、ブール型のプロパティ値は、チェック ボックスの状態を変更することで操作を説明します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="98ca9-125">チェック ボックスが最初に表示されると、MAPI は、既定のプロパティのセットを取得するために表示された表に関連付けられている**IMAPIProp**実装の**GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="98ca9-126">**DTBLCHECKBOX**構造体のプロパティ タグのプロパティのいずれかのマップ、そのプロパティの値がチェック ボックスの初期値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="98ca9-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="98ca9-127">チェック ボックス コントロールは、変更可能なことができます。</span><span class="sxs-lookup"><span data-stu-id="98ca9-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="98ca9-128">これにより、ユーザーの状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-128">This allows a user to change their states.</span></span> <span data-ttu-id="98ca9-129">変更可能] チェック ボックスは、 **ulCtlFlags** 、 [DTCTL](dtctl.md)構造体のメンバーでは、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) のプロパティに DT_EDITABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="98ca9-130">チェック ボックスの状態が変更されるとき、MAPI は、プロパティ タグの**DTBLCHECKBOX**構造体のメンバーを新しい状態で識別されるプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="98ca9-131">たとえば、アドレス帳プロバイダーと、受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティの設定を調整するのには、[構成] ダイアログ ボックスで、変更可能なチェック ボックス コントロール場合があります。</span><span class="sxs-lookup"><span data-stu-id="98ca9-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="98ca9-132">ユーザーは、チェック ボックスを選択すると、MAPI はこのプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="98ca9-133">チェック ボックスが選択されているプロパティが FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="98ca9-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="98ca9-134">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ca9-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="98ca9-135">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ca9-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="98ca9-136">プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ca9-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98ca9-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="98ca9-137">See also</span></span>



[<span data-ttu-id="98ca9-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="98ca9-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="98ca9-139">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98ca9-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="98ca9-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="98ca9-140">MAPI Structures</span></span>](mapi-structures.md)

