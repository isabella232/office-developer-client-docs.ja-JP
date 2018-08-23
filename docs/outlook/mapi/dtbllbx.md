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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569765"
---
# <a name="dtbllbx"></a><span data-ttu-id="19af7-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="19af7-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="19af7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19af7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19af7-105">ディスプレイ テーブルから組み込まれているダイアログ ボックスで使用するリストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="19af7-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19af7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="19af7-106">Header file:</span></span>  <br/> |<span data-ttu-id="19af7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19af7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="19af7-108">Members</span><span class="sxs-lookup"><span data-stu-id="19af7-108">Members</span></span>

 <span data-ttu-id="19af7-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="19af7-109">**ulFlags**</span></span>
  
> <span data-ttu-id="19af7-110">リストからの水平方向または垂直方向のスクロール バーを排除するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="19af7-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="19af7-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="19af7-111">The following flags can be set:</span></span>
    
<span data-ttu-id="19af7-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="19af7-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="19af7-113">水平スクロール バーは必要があります、ボックスの一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="19af7-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="19af7-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="19af7-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="19af7-115">垂直スクロール バーは必要があります、ボックスの一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="19af7-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="19af7-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="19af7-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="19af7-117">任意の型のプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="19af7-117">Property tag for a property of any type.</span></span> <span data-ttu-id="19af7-118">このプロパティは、 **ulPRTableTable**のメンバーで識別されるテーブル内の列のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="19af7-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="19af7-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="19af7-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="19af7-120">PT_OBJECT、 **OpenProperty**を使用して開くことができる種類のテーブルのプロパティのプロパティ タグを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19af7-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="19af7-121">テーブルに含める列の数は、リストの 1 つまたは複数選択リストがかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="19af7-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="19af7-122">**UlPRSetProperty**メンバーは、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) に設定されている場合は、一覧は、複数選択できます。</span><span class="sxs-lookup"><span data-stu-id="19af7-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19af7-123">注釈</span><span class="sxs-lookup"><span data-stu-id="19af7-123">Remarks</span></span>

<span data-ttu-id="19af7-124">**DTBLLBX**構造体では、複数のアイテムを表示して、ユーザーが 1 つまたは複数の項目を選択するようにするために使用されるコントロールの一覧について説明します。</span><span class="sxs-lookup"><span data-stu-id="19af7-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="19af7-125">メンバーの**ulPRSetProperty**と**ulPRTableName**のメンバーが連携します。テーブルから 1 つの値を選択すると、それに書き戻さ**ulPRSetProperty** ] ダイアログ ボックスが閉じられるとき。</span><span class="sxs-lookup"><span data-stu-id="19af7-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="19af7-126">フラグ値は、水平方向または垂直方向のスクロール バーをリストに表示するかどうを示します。</span><span class="sxs-lookup"><span data-stu-id="19af7-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="19af7-127">既定では、スクロール バーが必要な場合を表示の種類が存在します。</span><span class="sxs-lookup"><span data-stu-id="19af7-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="19af7-128">サービス プロバイダーには、水平スクロール バーを非表示にする MAPI_NO_HBAR と垂直スクロール バーを非表示にする MAPI_NO_VBAR を設定できます。</span><span class="sxs-lookup"><span data-stu-id="19af7-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="19af7-129">2 つのプロパティ タグのメンバーが連携して、ボックスの一覧で値を表示し、リスト内のアイテムを選択すると、対応するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="19af7-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="19af7-130">MAPI には、まず、一覧が表示されるとき、に、 **ulPRTableName**メンバーで識別されたテーブルを取得するための**IMAPIProp**実装の**OpenProperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19af7-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="19af7-131">テーブル内の列の数は、 **ulPRSetProperty**メンバーの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="19af7-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="19af7-132">**UlPRSetProperty**は、 **PR_NULL**に設定されている場合は、受信者、アドレス帳コンテナーである、メッセージの受信者テーブルまたは配布リストの内容のテーブルなどが含まれているオブジェクトを基に複数選択リストは、リスト。</span><span class="sxs-lookup"><span data-stu-id="19af7-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="19af7-133">複数選択リストのテーブルには、次の列を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="19af7-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="19af7-134">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="19af7-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="19af7-135">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="19af7-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="19af7-136">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="19af7-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="19af7-137">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) と、他の 5 つの複数値を持つ文字列プロパティの最大は、3 つの必須の列を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="19af7-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="19af7-138">**UlPRSetProperty**メンバーが**PR_NULL**に設定されていない場合、リスト、単一選択リストです。</span><span class="sxs-lookup"><span data-stu-id="19af7-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="19af7-139">**UlPRSetProperty**の初期値は、選択されている最初の行を決定します。</span><span class="sxs-lookup"><span data-stu-id="19af7-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="19af7-140">ユーザーは、行のいずれかを選択して**ulPRSetProperty**のメンバーは、選択した値に設定されてこの値が[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して、プロパティのインターフェイスの実装に書き戻す。</span><span class="sxs-lookup"><span data-stu-id="19af7-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="19af7-141">テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19af7-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="19af7-142">表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19af7-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19af7-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="19af7-143">See also</span></span>



[<span data-ttu-id="19af7-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="19af7-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="19af7-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="19af7-145">MAPI Structures</span></span>](mapi-structures.md)

