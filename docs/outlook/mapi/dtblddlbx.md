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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438849"
---
# <a name="dtblddlbx"></a><span data-ttu-id="f4503-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="f4503-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="f4503-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4503-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4503-105">表示テーブルから作成されたダイアログ ボックスで使用されるドロップダウン リスト コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f4503-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4503-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f4503-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4503-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4503-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="f4503-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="f4503-108">Members</span></span>

 <span data-ttu-id="f4503-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f4503-109">**ulFlags**</span></span>
  
> <span data-ttu-id="f4503-110">予約済みで、ゼロである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4503-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="f4503-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="f4503-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="f4503-112">型のプロパティのプロパティ タグPT_TSTRING。</span><span class="sxs-lookup"><span data-stu-id="f4503-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="f4503-113">このプロパティは、ulPRTableName メンバーによって識別されるテーブル **内の列の 1** つです。</span><span class="sxs-lookup"><span data-stu-id="f4503-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="f4503-114">このプロパティの値が一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4503-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="f4503-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="f4503-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="f4503-116">任意の種類のプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="f4503-116">Property tag for a property of any type.</span></span> <span data-ttu-id="f4503-117">このプロパティは、ulPRTableName メンバーによって識別されるテーブル **内の列の 1** つです。</span><span class="sxs-lookup"><span data-stu-id="f4503-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="f4503-118">リストのユーザーが **ulPRTableName** メンバーによって識別される表の行から **ulPRDisplayProperty** メンバーのプロパティ値を選択すると、対応する **ulPRSetProperty** メンバーが設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4503-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="f4503-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="f4503-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="f4503-120">**OpenProperty** 呼び出しを使用して開くことができるPT_OBJECTのテーブル プロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="f4503-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="f4503-121">表には **、ulPRDisplayProperty** と **ulPRSetProperty の 2 つの列が必要です**。</span><span class="sxs-lookup"><span data-stu-id="f4503-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="f4503-122">テーブルの行は、リスト内のアイテムに対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4503-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4503-123">注釈</span><span class="sxs-lookup"><span data-stu-id="f4503-123">Remarks</span></span>

<span data-ttu-id="f4503-124">**DTBLDDLBX** 構造体は、ユーザーが展開を選択するまで、1 つのアイテムとして表示されるドロップダウン リスト コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="f4503-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="f4503-125">プロパティ タグで識別される 3 つのプロパティは、一覧に情報を表示し、関連するプロパティを設定するために連携します。</span><span class="sxs-lookup"><span data-stu-id="f4503-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="f4503-126">**ulPRTableName** メンバーは [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しを介してアクセスされるテーブル オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="f4503-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="f4503-127">表には **、ulPRDisplayProperty** メンバーによって識別されるプロパティの列と **、ulPRSetProperty** メンバーによって識別されるプロパティの列の 2 つの列があります。</span><span class="sxs-lookup"><span data-stu-id="f4503-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="f4503-128">**ulPRDisplayProperty プロパティは**、リスト表示を駆動します。</span><span class="sxs-lookup"><span data-stu-id="f4503-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="f4503-129">ユーザーが表示から値の 1 つを選択すると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して、対応するプロパティを **ulPRSetProperty** メンバーによって識別される値として設定します。</span><span class="sxs-lookup"><span data-stu-id="f4503-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="f4503-130">これは、選択した表示プロパティと同じ行のプロパティを意味します。</span><span class="sxs-lookup"><span data-stu-id="f4503-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="f4503-131">**ulPRSetProperty メンバー** は、PR_NULL **(** [PidTagNull ) に設定できません](pidtagnull-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="f4503-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="f4503-132">MAPI が [IMAPIProp::GetProps](imapiprop-getprops.md)の呼び出しを通じて **ulPRSetProperty** メンバーによって表されるプロパティを取得し **、ulPRSetProperty** メンバーの値を持つテーブル内の行を見つけた場合、初期値がリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4503-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="f4503-133">最初に表示される値は、構造の **ulPRDisplayProperty** メンバーのプロパティに一致する、その行の **ulPRDisplayProperty** 列の内容です。</span><span class="sxs-lookup"><span data-stu-id="f4503-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="f4503-134">**ulPRDisplayProperty** メンバーによって識別されるプロパティの **GetProps** によって返される値は、リストが最初に表示されると表示される初期値になります。</span><span class="sxs-lookup"><span data-stu-id="f4503-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="f4503-135">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="f4503-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f4503-136">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="f4503-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="f4503-137">プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f4503-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4503-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4503-138">See also</span></span>



[<span data-ttu-id="f4503-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f4503-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="f4503-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f4503-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f4503-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="f4503-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="f4503-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f4503-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="f4503-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f4503-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="f4503-144">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="f4503-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="f4503-145">テーブルの表示</span><span class="sxs-lookup"><span data-stu-id="f4503-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="f4503-146">MAPI プロパティの種類の概要</span><span class="sxs-lookup"><span data-stu-id="f4503-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

