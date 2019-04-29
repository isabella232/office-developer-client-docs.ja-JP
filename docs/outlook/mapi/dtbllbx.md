---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438569"
---
# <a name="dtbllbx"></a><span data-ttu-id="81554-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="81554-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="81554-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81554-105">表示テーブルから構築されたダイアログボックスで使用されるリストを表します。</span><span class="sxs-lookup"><span data-stu-id="81554-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81554-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="81554-106">Header file:</span></span>  <br/> |<span data-ttu-id="81554-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81554-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="81554-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="81554-108">Members</span></span>

 <span data-ttu-id="81554-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="81554-109">**ulFlags**</span></span>
  
> <span data-ttu-id="81554-110">リストから水平または垂直スクロールバーを削除するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="81554-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="81554-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="81554-111">The following flags can be set:</span></span>
    
<span data-ttu-id="81554-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="81554-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="81554-113">リストに水平スクロールバーを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="81554-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="81554-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="81554-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="81554-115">リストに垂直スクロールバーを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="81554-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="81554-116">**ulprsetproperty**</span><span class="sxs-lookup"><span data-stu-id="81554-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="81554-117">任意の型のプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="81554-117">Property tag for a property of any type.</span></span> <span data-ttu-id="81554-118">このプロパティは、 **ulprtabletable**メンバーで識別されるテーブルの列の1つです。</span><span class="sxs-lookup"><span data-stu-id="81554-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="81554-119">**ulprtablename**</span><span class="sxs-lookup"><span data-stu-id="81554-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="81554-120">**openproperty**呼び出しを使用して開くことができる PT_OBJECT 型のテーブルプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="81554-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="81554-121">表に含める必要のある列の数は、リストが単一または複数の選択リストであるかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="81554-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="81554-122">**ulprsetproperty**メンバーが**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定されている場合、リストは複数の項目を選択できます。</span><span class="sxs-lookup"><span data-stu-id="81554-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81554-123">注釈</span><span class="sxs-lookup"><span data-stu-id="81554-123">Remarks</span></span>

<span data-ttu-id="81554-124">**dtbllbx**構造体は、複数のアイテムを表示するために使用されるコントロールのリストを記述し、ユーザーが1つ以上のアイテムを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="81554-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="81554-125">**ulprsetproperty**メンバーと**ulprsetproperty**メンバーは連携して動作します。テーブルから1つの値が選択されている場合、ダイアログボックスが閉じられたときに**ulprsetproperty**に書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="81554-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="81554-126">flags 値は、水平または垂直のスクロールバーを一覧と共に表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="81554-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="81554-127">既定では、必要に応じてスクロールバーの種類を表示します。</span><span class="sxs-lookup"><span data-stu-id="81554-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="81554-128">サービスプロバイダーは、MAPI_NO_HBAR を設定して、水平スクロールバーと MAPI_NO_VBAR を非表示にし、垂直スクロールバーを非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="81554-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="81554-129">2つのプロパティタグメンバーは連携してリスト内の値を表示し、リスト内の項目が選択されたときに対応するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81554-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="81554-130">MAPI が最初にリストを表示するときは、 **imapiprop**実装の**openproperty**メソッドを呼び出して、 **ulprtablename**メンバーで識別されたテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="81554-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="81554-131">テーブル内の列数は、 **ulprsetproperty**メンバーの値に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="81554-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="81554-132">**ulprsetproperty**が**PR_NULL**に設定されている場合、リストは、アドレス帳コンテナー、メッセージの受信者テーブル、配布リストのコンテンツテーブルなど、受信者を含むオブジェクトに基づいて複数の選択リストになります。</span><span class="sxs-lookup"><span data-stu-id="81554-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="81554-133">複数選択リストのテーブルには、次の列が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="81554-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="81554-134">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81554-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="81554-135">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81554-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="81554-136">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="81554-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="81554-137">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) およびその他の最大5つの複数値文字列プロパティを、3つの必須列と共に表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="81554-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="81554-138">**ulprsetproperty**メンバーが**PR_NULL**に設定されていない場合、リストは単一の選択一覧になります。</span><span class="sxs-lookup"><span data-stu-id="81554-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="81554-139">**ulprsetproperty**の初期値は、最初に選択された行を決定します。</span><span class="sxs-lookup"><span data-stu-id="81554-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="81554-140">ユーザーがいずれかの行を選択すると、 **ulprsetproperty**メンバーが選択された値に設定され、この値は、 [imapiprop:: setprops](imapiprop-setprops.md)を呼び出すことでプロパティインターフェイスの実装に書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="81554-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="81554-141">表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81554-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="81554-142">表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81554-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81554-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="81554-143">See also</span></span>



[<span data-ttu-id="81554-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="81554-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="81554-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="81554-145">MAPI Structures</span></span>](mapi-structures.md)

