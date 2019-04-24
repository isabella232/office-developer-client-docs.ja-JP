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
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330246"
---
# <a name="adrlist"></a><span data-ttu-id="2373c-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2373c-103">ADRLIST</span></span>

<span data-ttu-id="2373c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2373c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2373c-105">1つまたは複数の受信者に属する0個以上のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="2373c-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2373c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2373c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2373c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2373c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2373c-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="2373c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2373c-109">[cbadrlist](cbadrlist.md)、 [cbnewadrlist](cbnewadrlist.md)、 [cbnewadrlist](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="2373c-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="2373c-110">Members</span><span class="sxs-lookup"><span data-stu-id="2373c-110">Members</span></span>

<span data-ttu-id="2373c-111">**centries**</span><span class="sxs-lookup"><span data-stu-id="2373c-111">**cEntries**</span></span>
  
> <span data-ttu-id="2373c-112">**aentries**メンバーによって指定された配列内のエントリの数。</span><span class="sxs-lookup"><span data-stu-id="2373c-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="2373c-113">**aentries**</span><span class="sxs-lookup"><span data-stu-id="2373c-113">**aEntries**</span></span>
  
> <span data-ttu-id="2373c-114">[adrentry](adrentry.md)構造体の配列。各受信者の1つの構造体です。</span><span class="sxs-lookup"><span data-stu-id="2373c-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2373c-115">解説</span><span class="sxs-lookup"><span data-stu-id="2373c-115">Remarks</span></span>

<span data-ttu-id="2373c-116">**adrlist**構造体には、1つまたは複数の**adrlist**構造体が含まれており、それぞれが受信者のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="2373c-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="2373c-117">受信者は未解決の場合があります。</span><span class="sxs-lookup"><span data-stu-id="2373c-117">A recipient can be unresolved.</span></span> <span data-ttu-id="2373c-118">これは、プロパティ値の配列にエントリ識別子がないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="2373c-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="2373c-119">解決された受信者は **、\_PR ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2373c-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="2373c-120">通常、解決された受信者には、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) プロパティの電子メールアドレスもあります。</span><span class="sxs-lookup"><span data-stu-id="2373c-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="2373c-121">ただし、電子メールアドレスは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="2373c-121">However, the email address is not required.</span></span> <span data-ttu-id="2373c-122">**adrlist**構造体は、たとえば、送信メッセージの受信者の一覧を記述したり、MAPI でアドレス帳のエントリを表示したりするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2373c-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="2373c-123">**adrlist**構造は、[行セット](srowset.md)構造に似ています。テーブル内の行を表すために使用される構造。</span><span class="sxs-lookup"><span data-stu-id="2373c-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="2373c-124">実際には、これら2つの構造は、同じように使用できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="2373c-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="2373c-125">両方には、プロパティのグループと、配列内の値の数を記述する構造の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2373c-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="2373c-126">**adrlist**構造体には、配列に[adrlist](adrentry.md)構造体が含まれ\*\*\*\* ています。この配列には、srowset 構造体が含まれています。 [](srow.md)</span><span class="sxs-lookup"><span data-stu-id="2373c-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="2373c-127">レイアウトでは、 **adrentry**構造体と**srow**構造は同じです。</span><span class="sxs-lookup"><span data-stu-id="2373c-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="2373c-128">**adrlist**および**srowset**構造は同じ割り当てルールに従っているため、アドレス帳コンテナーの contents テーブルから取得される**srowset**構造は、 **adrlist**構造体にキャストして、その代わりに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2373c-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="2373c-129">次の図は、 **adrlist**構造のレイアウトを示しています。</span><span class="sxs-lookup"><span data-stu-id="2373c-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="2373c-130">**ADRLIST コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="2373c-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="2373c-131">![adrlist コンポーネント](media/amapi_18.gif "adrlist コンポーネント")</span><span class="sxs-lookup"><span data-stu-id="2373c-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="2373c-132">adrentry 構造体の**adrentry**および\*\*\*\* [spropvalue](spropvalue.md)の部分は、他の部分とは独立して割り当てられ、解放される必要があります。</span><span class="sxs-lookup"><span data-stu-id="2373c-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="2373c-133">つまり、adrentry 構造体を解放する前に、 **adrentry**構造体のメモリを割り当てて解放した後\*\*\*\* で、各**spropvalue**構造体を個別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2373c-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="2373c-134">このようにメモリを処理することで、受信者および個々の受信者のプロパティをアドレス一覧から自由に追加または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="2373c-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="2373c-135">**adrlist**構造体とそのすべての部分を割り当てて解放するには、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIFreeBuffer](mapifreebuffer.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2373c-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="2373c-136">受信者の一覧が大きすぎてメモリに入らない場合、クライアントは[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出して、リストのサブセットを操作することができます。</span><span class="sxs-lookup"><span data-stu-id="2373c-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="2373c-137">クライアントは、このような状況では、アドレス帳の共通ダイアログボックスを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2373c-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="2373c-138">**adrentry**構造にメモリを割り当てる方法の詳細については、「 [adrentry および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2373c-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2373c-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="2373c-139">See also</span></span>

- [<span data-ttu-id="2373c-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2373c-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="2373c-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="2373c-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="2373c-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="2373c-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="2373c-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2373c-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="2373c-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="2373c-144">MAPI Structures</span></span>](mapi-structures.md)

