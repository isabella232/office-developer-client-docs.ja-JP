---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421439"
---
# <a name="adrentry"></a><span data-ttu-id="41f7a-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="41f7a-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="41f7a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41f7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41f7a-105">受信者に属する 0 個以上のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="41f7a-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41f7a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="41f7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="41f7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41f7a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="41f7a-108">Members</span><span class="sxs-lookup"><span data-stu-id="41f7a-108">Members</span></span>

 <span data-ttu-id="41f7a-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="41f7a-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="41f7a-110">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="41f7a-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="41f7a-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="41f7a-111">**cValues**</span></span>
  
> <span data-ttu-id="41f7a-112">**rgPropVals** メンバーが指すプロパティ値配列内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="41f7a-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="41f7a-113">**cValues メンバーには** 0 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="41f7a-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="41f7a-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="41f7a-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="41f7a-115">受信者のプロパティを記述するプロパティ値配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="41f7a-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="41f7a-116">**rgPropVals メンバー** には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="41f7a-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="41f7a-117">注釈</span><span class="sxs-lookup"><span data-stu-id="41f7a-117">Remarks</span></span>

<span data-ttu-id="41f7a-118">**ADRENTRY 構造体は**、単一の受信者に属するプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="41f7a-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="41f7a-119">通常、受信者の説明に使用されるプロパティには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="41f7a-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="41f7a-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41f7a-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="41f7a-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41f7a-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="41f7a-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41f7a-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="41f7a-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41f7a-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="41f7a-124">受信者の [SPropValue](spropvalue.md) **配列に** PR_ENTRYID識別子またはプロパティが表示される場合、これは受信者が解決済みかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="41f7a-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="41f7a-125">クライアントは [、IAddrBook::ResolveName](iaddrbook-resolvename.md) メソッドを呼び出して、送信メッセージの受信者リスト内のすべての受信者が解決済みである必要があります。</span><span class="sxs-lookup"><span data-stu-id="41f7a-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="41f7a-126">メッセージと一緒に送信できるのは、解決された受信者のみです。</span><span class="sxs-lookup"><span data-stu-id="41f7a-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="41f7a-127">**ADRENTRY** 構造体は、通常、ADRLIST 構造体 **の aEntries** メンバーの [配列を形成するために結合](adrlist.md) されます。</span><span class="sxs-lookup"><span data-stu-id="41f7a-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="41f7a-128">**ADRENTRY** 構造体と [SRow](srow.md) 構造体は、予約メンバー、プロパティ値の配列、および配列内の値の数を含むため、同じです。</span><span class="sxs-lookup"><span data-stu-id="41f7a-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="41f7a-129">**ADRENTRY** 構造体が結合され **、ADRLIST** 構造体の **aEntries** メンバーが形成されるのに対し **、SRow** 構造体は結合して [SRowSet](srowset.md)構造体の **aRow** メンバーを形成します。</span><span class="sxs-lookup"><span data-stu-id="41f7a-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="41f7a-130">どちらの構造も同じ割り当てルールに従います。これは、アドレス帳コンテナーの目次テーブルから取得された **SRowSet** 構造体を **ADRLIST** 構造にキャストし、この方法で使用できることを示しています。</span><span class="sxs-lookup"><span data-stu-id="41f7a-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="41f7a-131">**ADRENTRY 構造体は** 空の場合があります。</span><span class="sxs-lookup"><span data-stu-id="41f7a-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="41f7a-132">たとえば **、IAddrBook::Address** の呼び出しで _lppAdrList_ パラメーターが指す **ADRLIST** 構造体に含まれる **ADRENTRY** 構造体は、受信者が削除されているときに空にできます。</span><span class="sxs-lookup"><span data-stu-id="41f7a-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="41f7a-133">**ADRENTRY** 構造体にメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41f7a-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41f7a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="41f7a-134">See also</span></span>



[<span data-ttu-id="41f7a-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="41f7a-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="41f7a-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="41f7a-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="41f7a-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="41f7a-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="41f7a-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="41f7a-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="41f7a-139">SRow</span><span class="sxs-lookup"><span data-stu-id="41f7a-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="41f7a-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="41f7a-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="41f7a-141">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="41f7a-141">MAPI Structures</span></span>](mapi-structures.md)

