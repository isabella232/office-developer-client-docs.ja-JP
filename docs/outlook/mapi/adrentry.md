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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19799669"
---
# <a name="adrentry"></a><span data-ttu-id="5c788-103">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="5c788-103">ADRENTRY</span></span>

  
  
<span data-ttu-id="5c788-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c788-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c788-105">受信者に所属する 0 個以上のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5c788-105">Describes zero or more properties that belong to a recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c788-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5c788-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c788-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c788-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a><span data-ttu-id="5c788-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="5c788-108">Members</span></span>

 <span data-ttu-id="5c788-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="5c788-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="5c788-110">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c788-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5c788-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="5c788-111">**cValues**</span></span>
  
> <span data-ttu-id="5c788-112">**RgPropVals**メンバーが指すプロパティの値の配列内のプロパティの数です。</span><span class="sxs-lookup"><span data-stu-id="5c788-112">Count of properties in the property value array pointed to by the **rgPropVals** member.</span></span> <span data-ttu-id="5c788-113">**あう**メンバーは、0 にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c788-113">The **cValues** member can be zero.</span></span> 
    
 <span data-ttu-id="5c788-114">**rgPropVals**</span><span class="sxs-lookup"><span data-stu-id="5c788-114">**rgPropVals**</span></span>
  
> <span data-ttu-id="5c788-115">受信者のプロパティを記述するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c788-115">Pointer to a property value array describing the properties for the recipient.</span></span> <span data-ttu-id="5c788-116">**RgPropVals**のメンバーには、NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5c788-116">The **rgPropVals** member can be NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c788-117">備考</span><span class="sxs-lookup"><span data-stu-id="5c788-117">Remarks</span></span>

<span data-ttu-id="5c788-118">**ADRENTRY**構造体では、1 人の受信者のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5c788-118">An **ADRENTRY** structure describes properties that belong to a single recipient.</span></span> <span data-ttu-id="5c788-119">受信者の記述に使用される一般的なプロパティを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="5c788-119">The properties that are typically used to describe a recipient include the following:</span></span> 
  
 <span data-ttu-id="5c788-120">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5c788-120">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
  
 <span data-ttu-id="5c788-121">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5c788-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
  
 <span data-ttu-id="5c788-122">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5c788-122">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
  
 <span data-ttu-id="5c788-123">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5c788-123">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="5c788-124">エントリの識別子または**PR_ENTRYID**プロパティが表示されたら[SPropValue](spropvalue.md)配列の受信者に、受信者が解決されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="5c788-124">When an entry identifier or **PR_ENTRYID** property appears in the [SPropValue](spropvalue.md) array for a recipient, this indicates that the recipient has been resolved.</span></span> <span data-ttu-id="5c788-125">クライアントは、送信メッセージの受信者の一覧のすべての受信者が解決されたことを確認するのには[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5c788-125">Clients call the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method to make sure that all recipients in the recipient list of an outgoing message have been resolved.</span></span> <span data-ttu-id="5c788-126">解決受信者のみにメッセージを送信できます。</span><span class="sxs-lookup"><span data-stu-id="5c788-126">Only resolved recipients can be sent with messages.</span></span> 
  
 <span data-ttu-id="5c788-127">**ADRENTRY**構造体は通常、 **aEntries** 、 [ADRLIST](adrlist.md)構造体のメンバーの配列を作成する結合します。</span><span class="sxs-lookup"><span data-stu-id="5c788-127">**ADRENTRY** structures are typically combined to form an array for the **aEntries** member of an [ADRLIST](adrlist.md) structure.</span></span> 
  
 <span data-ttu-id="5c788-128">**ADRENTRY**構造体および[SRow](srow.md)の構造体は、両方を含むので、予約済みのメンバー プロパティの値の配列、配列内の値の数と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c788-128">**ADRENTRY** structures and [SRow](srow.md) structures are identical because they both contain a reserved member, an array of property values, and a count of values in the array.</span></span> <span data-ttu-id="5c788-129">**ADRENTRY**構造体は、 **aEntries** 、 **ADRLIST**構造体のメンバーをフォームに組み合わせることで、一方、 **SRow**構造体は、 **aRow** 、 [SRowSet](srowset.md)構造体のメンバーをフォームに結合されます。</span><span class="sxs-lookup"><span data-stu-id="5c788-129">Whereas **ADRENTRY** structures are combined to form the **aEntries** member of an **ADRLIST** structure, **SRow** structures are combined to form the **aRow** member of an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="5c788-130">構造体の両方の種類は、アドレス帳コンテナーのコンテンツ テーブルから取得した**SRowSet**構造体の**ADRLIST**構造体へのキャストし、は、使用することを示す、同じ割り当て規則に従います。</span><span class="sxs-lookup"><span data-stu-id="5c788-130">Both types of structures follow the same allocation rules, implying that an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="5c788-131">**ADRENTRY**構造体を空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c788-131">An **ADRENTRY** structure can be empty.</span></span> <span data-ttu-id="5c788-132">たとえば、 **IAddrBook::Address**への呼び出し内の_lppAdrList_パラメーターで指定された**ADRLIST**構造体に含まれる**ADRENTRY**構造体は、受信者が削除されるときに空。</span><span class="sxs-lookup"><span data-stu-id="5c788-132">For example, an **ADRENTRY** structure that is contained in the **ADRLIST** structure pointed to by the  _lppAdrList_ parameter in a call to **IAddrBook::Address** can be empty when a recipient is being removed.</span></span> 
  
<span data-ttu-id="5c788-133">**ADRENTRY**構造体にメモリを割り当てる方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c788-133">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c788-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c788-134">See also</span></span>



[<span data-ttu-id="5c788-135">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="5c788-135">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="5c788-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="5c788-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="5c788-137">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5c788-137">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5c788-138">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="5c788-138">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="5c788-139">SRow</span><span class="sxs-lookup"><span data-stu-id="5c788-139">SRow</span></span>](srow.md)
  
[<span data-ttu-id="5c788-140">SRowSet</span><span class="sxs-lookup"><span data-stu-id="5c788-140">SRowSet</span></span>](srowset.md)


[<span data-ttu-id="5c788-141">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5c788-141">MAPI Structures</span></span>](mapi-structures.md)

