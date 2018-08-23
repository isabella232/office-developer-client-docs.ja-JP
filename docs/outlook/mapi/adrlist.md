---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b2d3dce7835f92d9ad78f7d8837e655fdd8fd412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799657"
---
# <a name="adrlist"></a><span data-ttu-id="ed5e4-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ed5e4-103">ADRLIST</span></span>

<span data-ttu-id="ed5e4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed5e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed5e4-105">1 つまたは複数の受信者に所属する 0 個以上のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5e4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ed5e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed5e4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed5e4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ed5e4-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="ed5e4-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ed5e4-109">[CbADRLIST](cbadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="ed5e4-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="ed5e4-110">Members</span><span class="sxs-lookup"><span data-stu-id="ed5e4-110">Members</span></span>

<span data-ttu-id="ed5e4-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="ed5e4-111">**cEntries**</span></span>
  
> <span data-ttu-id="ed5e4-112">**AEntries**メンバーによって指定された配列内のエントリの数です。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="ed5e4-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="ed5e4-113">**aEntries**</span></span>
  
> <span data-ttu-id="ed5e4-114">[ADRENTRY](adrentry.md)構造体の配列、各受信者の 1 つの構造体です。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ed5e4-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ed5e4-115">Remarks</span></span>

<span data-ttu-id="ed5e4-116">**ADRLIST**構造体は、各受信者のプロパティを記述する 1 つまたは複数の**ADRENTRY**構造体を格納します。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="ed5e4-117">受信者が解決することができます。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-117">A recipient can be unresolved.</span></span> <span data-ttu-id="ed5e4-118">これは、プロパティ値の配列内のエントリ識別子を欠けていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="ed5e4-119">受信者が解決されたことを意味します**PR\_エントリ ID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="ed5e4-120">通常、受信者の解決は、電子メール アドレス ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) である**PR_EMAIL_ADDRESS**プロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="ed5e4-121">ただし、電子メール アドレスは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-121">However, the email address is not required.</span></span> <span data-ttu-id="ed5e4-122">**ADRLIST**構造体は、たとえば、MAPI アドレス帳にエントリを表示するのには、送信メッセージの受信者の一覧を記述する使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="ed5e4-123">[SRowSet](srowset.md)構造体のテーブル内の行を表すために使用する構造体**ADRLIST**の構造と似ています。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="ed5e4-124">実際には、これら 2 つの構造体は、同じ意味で使用できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="ed5e4-125">両方には、プロパティのグループと、配列内の値の数を記述する構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="ed5e4-126">**ADRLIST**構造体の配列が含まれますが、 **SRowSet**構造体、配列内の[ADRENTRY](adrentry.md)の構造体には、 [SRow](srow.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="ed5e4-127">**ADRENTRY**構造体および**SRow**の構造体は、レイアウトでは同じです。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="ed5e4-128">**ADRLIST**と**SRowSet**構造体は、同じ割り当て規則に従う、ため、アドレス帳コンテナーのコンテンツ テーブルから取得した**SRowSet**構造体は**ADRLIST**構造体へのキャストし、そのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="ed5e4-129">次の図は、 **ADRLIST**構造体のレイアウトを示しています。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="ed5e4-130">**ADRLIST コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="ed5e4-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="ed5e4-131">![ADRLIST コンポーネント](media/amapi_18.gif "ADRLIST コンポーネント")</span><span class="sxs-lookup"><span data-stu-id="ed5e4-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="ed5e4-132">**ADRLIST**構造体の**ADRENTRY**と[SPropValue](spropvalue.md)の部分を割り当てられ、他の部分とは別に解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="ed5e4-133">つまり、各**SPropValue**構造体割り当てる必要があります個別に**ADRENTRY**構造体のメモリが割り当てられ、 **ADRENTRY**構造体が解放される前に解放された後。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="ed5e4-134">メモリを処理するときのこの独立性は、自由に追加または、[アドレス] ボックスの一覧から削除するには、受信者と受信者のプロパティを個別に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="ed5e4-135">割り当ておよび**ADRLIST**の構造とそのすべての部分を解放する[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIFreeBuffer](mapifreebuffer.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="ed5e4-136">受信者の一覧がメモリに収まるように大きすぎる場合は、クライアントは、リストのサブセットを処理する[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="ed5e4-137">クライアントでは、アドレス帳コモン ダイアログ ボックスでこのような場合は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="ed5e4-138">**ADRENTRY**構造体にメモリを割り当てる方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed5e4-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed5e4-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed5e4-139">See also</span></span>

- [<span data-ttu-id="ed5e4-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ed5e4-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="ed5e4-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="ed5e4-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="ed5e4-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ed5e4-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="ed5e4-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ed5e4-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="ed5e4-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ed5e4-144">MAPI Structures</span></span>](mapi-structures.md)

