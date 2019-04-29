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
# <a name="dtblddlbx"></a><span data-ttu-id="e9d5f-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="e9d5f-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="e9d5f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9d5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9d5f-105">表示テーブルから構築されたダイアログボックスで使用されるドロップダウンリストコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d5f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9d5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9d5f-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9d5f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="e9d5f-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="e9d5f-108">Members</span></span>

 <span data-ttu-id="e9d5f-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e9d5f-109">**ulFlags**</span></span>
  
> <span data-ttu-id="e9d5f-110">予約済み。0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="e9d5f-111">**ulprdisplayproperty**</span><span class="sxs-lookup"><span data-stu-id="e9d5f-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="e9d5f-112">PT_TSTRING 型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="e9d5f-113">このプロパティは、 **ulprtablename**メンバーによって識別されるテーブルの列の1つです。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e9d5f-114">このプロパティの値は、一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="e9d5f-115">**ulprsetproperty**</span><span class="sxs-lookup"><span data-stu-id="e9d5f-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="e9d5f-116">任意の型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-116">Property tag for a property of any type.</span></span> <span data-ttu-id="e9d5f-117">このプロパティは、 **ulprtablename**メンバーによって識別されるテーブルの列の1つです。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e9d5f-118">リストのユーザーが ulprtablename メンバーによって識別されるテーブルの行から**ulprdisplayproperty**メンバーのプロパティ値\*\*\*\* を選択すると、対応する**ulprsetproperty**メンバーが設定されます。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="e9d5f-119">**ulprtablename**</span><span class="sxs-lookup"><span data-stu-id="e9d5f-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="e9d5f-120">**openproperty**呼び出しを使用して開くことができる PT_OBJECT 型のテーブルプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="e9d5f-121">このテーブルには2つの列を指定する必要があります。 **ulprdisplayproperty**および**ulprsetproperty**。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="e9d5f-122">表の行は、リスト内の項目に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9d5f-123">注釈</span><span class="sxs-lookup"><span data-stu-id="e9d5f-123">Remarks</span></span>

<span data-ttu-id="e9d5f-124">**dtblddlbx**構造体は、ユーザーがそれを展開することになるまで、1つのアイテムとして表示されるドロップダウンリストコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="e9d5f-125">プロパティタグによって識別される3つのプロパティが連携して、リスト内の情報を表示し、関連するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="e9d5f-126">**ulprtablename**メンバーは、 [imapiprop:: openproperty](imapiprop-openproperty.md)への呼び出しによってアクセスされる table オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="e9d5f-127">このテーブルには2つの列があります。 **ulprdisplayproperty**メンバーによって識別されるプロパティの1つの列と、 **ulprsetproperty**メンバーによって識別されるプロパティの列は1つです。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="e9d5f-128">**ulprdisplayproperty**プロパティは、リスト表示を駆動します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="e9d5f-129">ユーザーが表示から値の1つを選択すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、 **ulprsetproperty**メンバーによって識別される対応するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e9d5f-130">これは、プロパティが選択した表示プロパティと同じ行にあることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="e9d5f-131">**ulprsetproperty**メンバーを**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="e9d5f-132">MAPI が、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して**ulprsetproperty**メンバーによって表されるプロパティを取得し、テーブルの行に**ulprsetproperty**メンバーの値を格納している場合は、リストに初期値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e9d5f-133">最初に表示される値は、構造体の**ulprdisplayproperty**メンバーのプロパティに一致する行からの**ulprdisplayproperty**列の内容です。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="e9d5f-134">**ulprdisplayproperty**メンバーによって識別されるプロパティの**GetProps**によって返される値は、リストが最初に表示されたときに表示される初期値になります。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="e9d5f-135">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e9d5f-136">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="e9d5f-137">プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9d5f-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9d5f-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9d5f-138">See also</span></span>



[<span data-ttu-id="e9d5f-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e9d5f-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="e9d5f-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e9d5f-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e9d5f-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e9d5f-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e9d5f-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e9d5f-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="e9d5f-143">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e9d5f-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="e9d5f-144">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="e9d5f-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="e9d5f-145">表の表示</span><span class="sxs-lookup"><span data-stu-id="e9d5f-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="e9d5f-146">MAPI プロパティの種類の概要</span><span class="sxs-lookup"><span data-stu-id="e9d5f-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

