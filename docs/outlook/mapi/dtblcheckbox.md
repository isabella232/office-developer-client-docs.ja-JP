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
# <a name="dtblcheckbox"></a><span data-ttu-id="9b5e1-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="9b5e1-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="9b5e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b5e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b5e1-105">表示テーブルから構築されたダイアログボックスで使用されるチェックボックスに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b5e1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9b5e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b5e1-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b5e1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9b5e1-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="9b5e1-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9b5e1-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="9b5e1-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="9b5e1-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="9b5e1-110">Members</span></span>

 <span data-ttu-id="9b5e1-111">**ulblpszlabel**</span><span class="sxs-lookup"><span data-stu-id="9b5e1-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="9b5e1-112">チェックボックスと共に表示される文字列のメモリ内での位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="9b5e1-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9b5e1-113">**ulFlags**</span></span>
  
> <span data-ttu-id="9b5e1-114">チェックボックスラベルの書式を指定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="9b5e1-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-115">The following flag can be set:</span></span>
    
<span data-ttu-id="9b5e1-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b5e1-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9b5e1-117">ラベルは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-117">The label is in Unicode format.</span></span> <span data-ttu-id="9b5e1-118">MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="9b5e1-119">**ulprpropertyname**</span><span class="sxs-lookup"><span data-stu-id="9b5e1-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="9b5e1-120">PT_BOOLEAN 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="9b5e1-121">このプロパティの値は、チェックボックスの状態によって影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b5e1-122">注釈</span><span class="sxs-lookup"><span data-stu-id="9b5e1-122">Remarks</span></span>

<span data-ttu-id="9b5e1-123">**dtblcheckbox**構造体は、2つの状態 (オンボックス) または無効 (空のボックス) のいずれかを反映するコントロールのチェックボックスを記述します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="9b5e1-124">**ulprpropertyname**メンバーは、チェックボックスの状態を変更することによって値を操作する Boolean プロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="9b5e1-125">チェックボックスが最初に表示されると、MAPI は、表示テーブルに関連付けられている**imapiprop**実装の**GetProps**メソッドを呼び出して、一連の既定のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="9b5e1-126">プロパティのいずれかが**dtblcheckbox**構造体の property タグにマップされている場合、そのプロパティの値はチェックボックスの初期値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="9b5e1-127">チェックボックスコントロールを変更できます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="9b5e1-128">これにより、ユーザーは自分の状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-128">This allows a user to change their states.</span></span> <span data-ttu-id="9b5e1-129">変更可能なチェックボックスでは、 [DTCTL](dtctl.md)構造の**ulCtlFlags**メンバーおよび**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに DT_EDITABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="9b5e1-130">チェックボックスの状態が変化すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、 **dtblcheckbox**構造のプロパティタグメンバーで識別されたプロパティを新しい状態に設定します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="9b5e1-131">たとえば、アドレス帳プロバイダーでは、受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティの設定を調整するために、変更可能なチェックボックスコントロールを構成ダイアログボックスに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="9b5e1-132">ユーザーがチェックボックスをオンにすると、MAPI はこのプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="9b5e1-133">チェックボックスが選択されていない場合、このプロパティは FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="9b5e1-134">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="9b5e1-135">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="9b5e1-136">プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b5e1-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b5e1-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b5e1-137">See also</span></span>



[<span data-ttu-id="9b5e1-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="9b5e1-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="9b5e1-139">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b5e1-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="9b5e1-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9b5e1-140">MAPI Structures</span></span>](mapi-structures.md)

