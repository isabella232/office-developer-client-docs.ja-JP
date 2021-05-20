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
# <a name="dtbllbx"></a><span data-ttu-id="a33e5-103">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="a33e5-103">DTBLLBX</span></span>

  
  
<span data-ttu-id="a33e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a33e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a33e5-105">表示テーブルから作成されたダイアログ ボックスで使用されるリストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-105">Describes a list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a33e5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a33e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="a33e5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a33e5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a><span data-ttu-id="a33e5-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="a33e5-108">Members</span></span>

 <span data-ttu-id="a33e5-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a33e5-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a33e5-110">リストから水平または垂直のスクロール バーを削除するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a33e5-110">Bitmask of flags used to eliminate a horizontal or vertical scroll bar from the list.</span></span> <span data-ttu-id="a33e5-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a33e5-112">MAPI_NO_HBAR</span><span class="sxs-lookup"><span data-stu-id="a33e5-112">MAPI_NO_HBAR</span></span> 
  
> <span data-ttu-id="a33e5-113">リストに水平スクロール バーを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a33e5-113">No horizontal scroll bar should be shown with the list.</span></span>
    
<span data-ttu-id="a33e5-114">MAPI_NO_VBAR</span><span class="sxs-lookup"><span data-stu-id="a33e5-114">MAPI_NO_VBAR</span></span> 
  
> <span data-ttu-id="a33e5-115">リストに垂直スクロール バーを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a33e5-115">No vertical scroll bar should be shown with the list.</span></span>
    
 <span data-ttu-id="a33e5-116">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="a33e5-116">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="a33e5-117">任意の種類のプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="a33e5-117">Property tag for a property of any type.</span></span> <span data-ttu-id="a33e5-118">このプロパティは、ulPRTableTable メンバーによって識別されるテーブル **内の列の 1** つです。</span><span class="sxs-lookup"><span data-stu-id="a33e5-118">This property is one of the columns in the table identified by the **ulPRTableTable** member.</span></span> 
    
 <span data-ttu-id="a33e5-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="a33e5-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="a33e5-120">**OpenProperty** 呼び出しを使用して開くことができるPT_OBJECTのテーブル プロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="a33e5-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="a33e5-121">テーブルに含む列の数は、リストが 1 つの選択リストか複数選択リストかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a33e5-121">The number of columns that the table should have depends on whether the list is a single or multiple selection list.</span></span> <span data-ttu-id="a33e5-122">**ulPRSetProperty** メンバーが PR_NULL **(** [PidTagNull)](pidtagnull-canonical-property.md)に設定されている場合、リストでは複数の選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="a33e5-122">If the **ulPRSetProperty** member is set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), the list allows for multiple selection.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a33e5-123">注釈</span><span class="sxs-lookup"><span data-stu-id="a33e5-123">Remarks</span></span>

<span data-ttu-id="a33e5-124">**DTBLLBX** 構造は、複数のアイテムを表示し、ユーザーが 1 つ以上のアイテムを選択するために使用するコントロールをリストに記述します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-124">A **DTBLLBX** structure describes a list a control that is used to show multiple items and let a user select one or more of the items.</span></span> 
  
<span data-ttu-id="a33e5-125">**ulPRSetProperty メンバーと** **ulPRTableName** メンバーが一緒に動作します。テーブルから 1 つの値を選択すると、ダイアログ ボックスが閉じらば **ulPRSetProperty** に書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-125">The **ulPRSetProperty** member and **ulPRTableName** member work together; when one value is chosen from the table, it is written back to **ulPRSetProperty** when the dialog box is dismissed.</span></span> 
  
<span data-ttu-id="a33e5-126">flags 値は、水平スクロール バーと垂直スクロール バーをリストと一緒に表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-126">The flags value indicates whether a horizontal or vertical scroll bar should be displayed with the list.</span></span> <span data-ttu-id="a33e5-127">既定では、必要に応じてスクロール バーの種類が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-127">The default is to have types of scroll bars appear if it is required.</span></span> <span data-ttu-id="a33e5-128">サービス プロバイダーは、水平方向MAPI_NO_HBARを抑制し、垂直スクロール バーを非表示MAPI_NO_VBARを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-128">Service providers can set MAPI_NO_HBAR to suppress a horizontal scroll bar and MAPI_NO_VBAR to suppress a vertical scroll bar.</span></span> 
  
<span data-ttu-id="a33e5-129">2 つのプロパティ タグ メンバーが連携して、リスト内の値を表示し、リスト内のアイテムが選択されている場合に対応するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-129">The two property tag members work together to display values in the list and set corresponding properties when an item in the list is selected.</span></span> <span data-ttu-id="a33e5-130">MAPI が最初にリストを表示すると **、IMAPIProp 実装** の **OpenProperty** メソッドを呼び出して **、ulPRTableName** メンバーで識別されたテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-130">When MAPI first displays the list, it calls the **IMAPIProp** implementation's **OpenProperty** method to retrieve the table identified in the **ulPRTableName** member.</span></span> <span data-ttu-id="a33e5-131">表内の列数は **、ulPRSetProperty** メンバーの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a33e5-131">The number of columns in the table depends on the value of the **ulPRSetProperty** member.</span></span> <span data-ttu-id="a33e5-132">**ulPRSetProperty** が **PR_NULL** に設定されている場合、リストは、アドレス帳コンテナー、メッセージの受信者テーブル、配布リストのコンテンツ テーブルなど、受信者を含むオブジェクトに基づく複数の選択リストです。</span><span class="sxs-lookup"><span data-stu-id="a33e5-132">If **ulPRSetProperty** is set to **PR_NULL**, the list is a multiple selection list based on an object that contains recipients, such as an address book container, a recipient table for a message, or a distribution list contents table.</span></span> 
  
<span data-ttu-id="a33e5-133">複数の選択リストのテーブルには、次の列が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a33e5-133">A table for a multiple selection list must include the following columns:</span></span>
  
 <span data-ttu-id="a33e5-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a33e5-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="a33e5-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a33e5-135">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
 <span data-ttu-id="a33e5-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a33e5-136">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
  
 <span data-ttu-id="a33e5-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) および最大 5 つの他の複数値文字列プロパティを、必要な 3 つの列と一緒に表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-137">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) and a maximum of five other multivalued string properties can also be displayed with the three required columns.</span></span> 
  
<span data-ttu-id="a33e5-138">**ulPRSetProperty** メンバーが設定されていない場合PR_NULLリストは 1 つの選択リストです。</span><span class="sxs-lookup"><span data-stu-id="a33e5-138">If the **ulPRSetProperty** member is not set to **PR_NULL**, the list is a single selection list.</span></span> <span data-ttu-id="a33e5-139">**ulPRSetProperty の初期値は**、最初に選択した行を決定します。</span><span class="sxs-lookup"><span data-stu-id="a33e5-139">The initial value of **ulPRSetProperty** determines the first selected row.</span></span> <span data-ttu-id="a33e5-140">ユーザーが行のいずれかを選択すると **、ulPRSetProperty** メンバーが選択した値に設定され、この値は [IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出してプロパティ インターフェイスの実装に書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="a33e5-140">When a user selects one of the rows, the **ulPRSetProperty** member is set to the selected value and this value is written back to the property interface implementation with a call to [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span> 
  
<span data-ttu-id="a33e5-141">表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="a33e5-141">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a33e5-142">表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="a33e5-142">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a33e5-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="a33e5-143">See also</span></span>



[<span data-ttu-id="a33e5-144">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a33e5-144">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="a33e5-145">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a33e5-145">MAPI Structures</span></span>](mapi-structures.md)

