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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330227"
---
# <a name="adrentry"></a><span data-ttu-id="54588-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="54588-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="54588-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54588-105">受信者に属する0個以上のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="54588-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54588-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="54588-106">Header file:</span></span>  <br/> |<span data-ttu-id="54588-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54588-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="54588-108">Members</span><span class="sxs-lookup"><span data-stu-id="54588-108">Members</span></span>

 <span data-ttu-id="54588-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="54588-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="54588-110">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="54588-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="54588-111">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="54588-111">**cValues**</span></span>
  
> <span data-ttu-id="54588-112">**rgPropVals**メンバーによって参照されているプロパティ値配列のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="54588-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="54588-113">**cvalues**メンバーは0にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54588-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="54588-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="54588-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="54588-115">受信者のプロパティを説明するプロパティ値配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="54588-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="54588-116">**rgPropVals**メンバーは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54588-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54588-117">解説</span><span class="sxs-lookup"><span data-stu-id="54588-117">Remarks</span></span>

<span data-ttu-id="54588-118">**adrentry**構造は、1人の受信者に属するプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="54588-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="54588-119">通常、受信者を表すために使用されるプロパティには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="54588-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="54588-120">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54588-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="54588-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54588-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="54588-122">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54588-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="54588-123">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="54588-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="54588-124">受信者の[spropvalue](spropvalue.md)配列にエントリ識別子または**PR_ENTRYID**プロパティが表示される場合、これは受信者が解決されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="54588-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="54588-125">クライアントは[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドを呼び出して、送信メッセージの受信者一覧内のすべての受信者が解決されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="54588-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="54588-126">解決された受信者のみがメッセージと共に送信できます。</span><span class="sxs-lookup"><span data-stu-id="54588-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="54588-127">通常、 **adrentry**構造体は、 [adrentry](adrlist.md)構造体の**aentries**メンバーの配列を形成するために組み合わされています。</span><span class="sxs-lookup"><span data-stu-id="54588-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="54588-128">**adrentry**構造体と[srow](srow.md)構造体の両方には、予約済みのメンバー、プロパティ値の配列、および配列内の値の数が含まれているため、同一です。</span><span class="sxs-lookup"><span data-stu-id="54588-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="54588-129">**adrentry**構造体は**adrentry**構造体の**aentries**メンバーを形成するために組み合わされていますが、 **srow**構造体は、 [srow](srowset.md)構造の**arow**メンバーを形成するために組み合わされています。</span><span class="sxs-lookup"><span data-stu-id="54588-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="54588-130">両方の種類の構造体は同じ割り当てルールに従い、アドレス帳コンテナーの contents テーブルから取得された**srowset**構造を**adrlist**構造体にキャストして、そのものとして使用できるということを意味します。</span><span class="sxs-lookup"><span data-stu-id="54588-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="54588-131">**adrentry**構造は空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54588-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="54588-132">たとえば、lppadrlist パラメーターによって指定さ\*\*\*\* れた adrentry 構造が、 **IAddrBook::** の呼び出しで\*\*\*\* _lppadrlist_パラメーターによって指定されている場合は、受信者が削除されているときに空になることがあります。</span><span class="sxs-lookup"><span data-stu-id="54588-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="54588-133">**adrentry**構造にメモリを割り当てる方法の詳細については、「 [adrentry および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54588-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54588-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="54588-134">See also</span></span>



[<span data-ttu-id="54588-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="54588-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="54588-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="54588-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="54588-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="54588-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="54588-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="54588-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="54588-139">SRow</span><span class="sxs-lookup"><span data-stu-id="54588-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="54588-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="54588-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="54588-141">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="54588-141">MAPI Structures</span></span>](mapi-structures.md)

