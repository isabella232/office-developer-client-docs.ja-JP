---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3307bb252ca4436999a541f85657fed9878c798a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579397"
---
# <a name="dtblddlbx"></a><span data-ttu-id="4b798-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="4b798-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="4b798-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b798-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b798-105">ダイアログ ボックスが表示テーブルの構築に使用するドロップダウン リスト コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b798-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b798-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4b798-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b798-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b798-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="4b798-108">Members</span><span class="sxs-lookup"><span data-stu-id="4b798-108">Members</span></span>

 <span data-ttu-id="4b798-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4b798-109">**ulFlags**</span></span>
  
> <span data-ttu-id="4b798-110">予約済み、0 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4b798-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="4b798-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="4b798-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="4b798-112">型 PT_TSTRING のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="4b798-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="4b798-113">このプロパティは、 **ulPRTableName**のメンバーで識別されるテーブル内の列のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4b798-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="4b798-114">このプロパティの値は、一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b798-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="4b798-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="4b798-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="4b798-116">任意の型のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="4b798-116">Property tag for a property of any type.</span></span> <span data-ttu-id="4b798-117">このプロパティは、 **ulPRTableName**のメンバーで識別されるテーブル内の列のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4b798-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="4b798-118">**UlPRTableName**メンバーで識別されるテーブルの行から**ulPRDisplayProperty**のメンバーのリストのユーザーがプロパティの値を選択すると、対応する**ulPRSetProperty**のメンバーが設定されます。</span><span class="sxs-lookup"><span data-stu-id="4b798-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="4b798-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="4b798-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="4b798-120">PT_OBJECT、 **OpenProperty**を使用して開くことができる種類のテーブルのプロパティのプロパティ タグを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4b798-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="4b798-121">テーブルが 2 つの列を持つ必要があります: **ulPRDisplayProperty**と**ulPRSetProperty**。</span><span class="sxs-lookup"><span data-stu-id="4b798-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="4b798-122">テーブルの行は、リスト内の項目に対応します。</span><span class="sxs-lookup"><span data-stu-id="4b798-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b798-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4b798-123">Remarks</span></span>

<span data-ttu-id="4b798-124">**DTBLDDLBX**構造体では、展開するまでに、1 つの項目として表示されているドロップダウン リスト コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b798-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="4b798-125">プロパティ タグで識別される 3 つのプロパティが連携する情報が一覧に表示し、関連するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4b798-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="4b798-126">**UlPRTableName**メンバーは、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出すことによってアクセスされているテーブル オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="4b798-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="4b798-127">テーブルには 2 つの列: **ulPRDisplayProperty**メンバーと**ulPRSetProperty**のメンバーによって識別されるプロパティによって識別されるプロパティの 1 つの列です。</span><span class="sxs-lookup"><span data-stu-id="4b798-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="4b798-128">**UlPRDisplayProperty**プロパティは、リストの表示をドライブします。</span><span class="sxs-lookup"><span data-stu-id="4b798-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="4b798-129">ユーザーは、表示値のいずれかを選択すると、MAPI は、 **ulPRSetProperty**のメンバーで識別される、対応するプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4b798-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="4b798-130">つまり、選択した表示のプロパティとして同じ行のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4b798-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="4b798-131">**UlPRSetProperty**メンバーは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定できません。</span><span class="sxs-lookup"><span data-stu-id="4b798-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="4b798-132">初期値は、MAPI が[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことによって**ulPRSetProperty**のメンバーによって表されるプロパティを取得し、 **ulPRSetProperty**メンバーの値を持つテーブルの行を配置する場合、一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b798-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="4b798-133">最初に表示される値は、 **ulPRDisplayProperty** 、 **ulPRDisplayProperty**構造体のメンバーのプロパティに一致する行をその列の内容です。</span><span class="sxs-lookup"><span data-stu-id="4b798-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="4b798-134">リストが最初に表示されるときに表示される初期値を**GetProps** **ulPRDisplayProperty**メンバーで識別されるプロパティの戻り値になります。</span><span class="sxs-lookup"><span data-stu-id="4b798-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="4b798-135">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b798-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="4b798-136">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b798-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="4b798-137">プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b798-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b798-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b798-138">See also</span></span>



[<span data-ttu-id="4b798-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="4b798-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="4b798-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="4b798-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="4b798-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="4b798-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="4b798-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4b798-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="4b798-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="4b798-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="4b798-144">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="4b798-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="4b798-145">表示テーブル</span><span class="sxs-lookup"><span data-stu-id="4b798-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="4b798-146">MAPI プロパティの型の概要</span><span class="sxs-lookup"><span data-stu-id="4b798-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

