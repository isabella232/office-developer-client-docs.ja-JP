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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415916"
---
# <a name="adrlist"></a><span data-ttu-id="9c417-103">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9c417-103">ADRLIST</span></span>

<span data-ttu-id="9c417-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c417-105">1 つ以上の受信者に属する 0 個以上のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9c417-105">Describes zero or more properties that belong to one or more recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c417-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9c417-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c417-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c417-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9c417-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="9c417-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9c417-109">[CbADRLIST](cbadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md)、 [CbNewADRLIST](cbnewadrlist.md)</span><span class="sxs-lookup"><span data-stu-id="9c417-109">[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md)</span></span> <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a><span data-ttu-id="9c417-110">Members</span><span class="sxs-lookup"><span data-stu-id="9c417-110">Members</span></span>

<span data-ttu-id="9c417-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="9c417-111">**cEntries**</span></span>
  
> <span data-ttu-id="9c417-112">**aEntries** メンバーで指定された配列内のエントリの数。</span><span class="sxs-lookup"><span data-stu-id="9c417-112">Count of entries in the array specified by the **aEntries** member.</span></span> 
    
<span data-ttu-id="9c417-113">**aEntries**</span><span class="sxs-lookup"><span data-stu-id="9c417-113">**aEntries**</span></span>
  
> <span data-ttu-id="9c417-114">[ADRENTRY 構造体の配列](adrentry.md)。受信者ごとに 1 つの構造。</span><span class="sxs-lookup"><span data-stu-id="9c417-114">Array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9c417-115">注釈</span><span class="sxs-lookup"><span data-stu-id="9c417-115">Remarks</span></span>

<span data-ttu-id="9c417-116">**ADRLIST 構造体には** 1 つ以上の **ADRENTRY** 構造が含まれています。それぞれが受信者のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="9c417-116">An **ADRLIST** structure contains one or more **ADRENTRY** structures, each describing the properties of a recipient.</span></span> <span data-ttu-id="9c417-117">受信者は未解決にできます。</span><span class="sxs-lookup"><span data-stu-id="9c417-117">A recipient can be unresolved.</span></span> <span data-ttu-id="9c417-118">つまり、プロパティ値の配列にエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9c417-118">This means that it is lacking an entry identifier in its array of property values.</span></span> <span data-ttu-id="9c417-119">解決済み受信者は **、PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが含まれるという意味です。</span><span class="sxs-lookup"><span data-stu-id="9c417-119">A resolved recipient means that the **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included.</span></span> <span data-ttu-id="9c417-120">通常、解決済み受信者には、電子メール アドレス [(PidTagEmailAddress](pidtagemailaddress-canonical-property.md) **)** プロパティPR_EMAIL_ADDRESSアドレスが設定されています。</span><span class="sxs-lookup"><span data-stu-id="9c417-120">Typically, resolved recipients also have an email address the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="9c417-121">ただし、電子メール アドレスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9c417-121">However, the email address is not required.</span></span> <span data-ttu-id="9c417-122">**ADRLIST 構造体** は、たとえば、送信メッセージの受信者リストを記述し、MAPI によってアドレス帳にエントリを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c417-122">**ADRLIST** structures are used, for example, to describe the recipient list for an outgoing message and by MAPI to display the entries in the address book.</span></span> 
  
<span data-ttu-id="9c417-123">**ADRLIST 構造体** は [、テーブル内の行を](srowset.md) 表す場合に使用される SRowSet 構造体に似た構造です。</span><span class="sxs-lookup"><span data-stu-id="9c417-123">**ADRLIST** structures resemble [SRowSet](srowset.md) structures the structures used for representing rows in tables.</span></span> <span data-ttu-id="9c417-124">実際、これら 2 つの構造は、同じ意味で使用できるよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="9c417-124">In fact, these two structures are designed so that they can be used interchangeably.</span></span> <span data-ttu-id="9c417-125">両方とも、プロパティのグループと配列内の値の数を記述する構造体の配列を含む。</span><span class="sxs-lookup"><span data-stu-id="9c417-125">Both contain an array of structures describing a group of properties and a count of the values in the array.</span></span> <span data-ttu-id="9c417-126">**ADRLIST 構造体では、配列** には [ADRENTRY](adrentry.md)構造体が含まれていますが **、SRowSet** 構造体には [SRow 構造体が含](srow.md)まれています。</span><span class="sxs-lookup"><span data-stu-id="9c417-126">Whereas in the **ADRLIST** structure, the array contains [ADRENTRY](adrentry.md) structures, in the **SRowSet** structure the array contains [SRow](srow.md) structures.</span></span> <span data-ttu-id="9c417-127">**ADRENTRY 構造** と **SRow 構造体** は、レイアウトで同じです。</span><span class="sxs-lookup"><span data-stu-id="9c417-127">**ADRENTRY** structures and **SRow** structures are identical in layout.</span></span> <span data-ttu-id="9c417-128">**ADRLIST** 構造体と **SRowSet** 構造体は同じ割り当てルールに従うので、アドレス帳コンテナーの目次テーブルから取得される **SRowSet** 構造体を **ADRLIST** 構造にキャストし、この形式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c417-128">Because **ADRLIST** and **SRowSet** structures follow the same allocation rules, an **SRowSet** structure that is retrieved from the contents table of an address book container can be cast to an **ADRLIST** structure and used as is.</span></span> 
  
<span data-ttu-id="9c417-129">次の図は **、ADRLIST 構造のレイアウトを示** しています。</span><span class="sxs-lookup"><span data-stu-id="9c417-129">The following illustration shows the layout of an **ADRLIST** structure.</span></span> 
  
<span data-ttu-id="9c417-130">**ADRLIST コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="9c417-130">**ADRLIST components**</span></span>
  
<span data-ttu-id="9c417-131">![ADRLIST コンポーネント](media/amapi_18.gif "ADRLIST コンポーネント")</span><span class="sxs-lookup"><span data-stu-id="9c417-131">![ADRLIST components](media/amapi_18.gif "ADRLIST components")</span></span>
  
<span data-ttu-id="9c417-132">**ADRLIST 構造体の ADRENTRY** 部分と [SPropValue](spropvalue.md)部分は、他の部分とは別に割り当て、解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c417-132">The **ADRENTRY** and [SPropValue](spropvalue.md) portions in an **ADRLIST** structure must be allocated and freed independently of the other parts.</span></span> <span data-ttu-id="9c417-133">つまり **、ADRENTRY** 構造体のメモリが割り当てられた後 **、ADRENTRY** 構造体を解放する前に、各 SPropValue 構造体を個別に割り当てる必要があります。 </span><span class="sxs-lookup"><span data-stu-id="9c417-133">That is, each **SPropValue** structure must be allocated individually after memory for the **ADRENTRY** structure has been allocated and freed before the **ADRENTRY** structure is freed.</span></span> <span data-ttu-id="9c417-134">このメモリ処理の独立性により、受信者と個々の受信者プロパティをアドレス一覧から自由に追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="9c417-134">This independence in handling memory allows recipients and individual recipient properties to be freely added or deleted from the address list.</span></span> 
  
<span data-ttu-id="9c417-135">**ADRLIST** 構造体とそのすべての部分を割り当て、解放するには [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIFreeBuffer](mapifreebuffer.md)関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c417-135">The [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions must be used to allocate and free the **ADRLIST** structure and all its parts.</span></span> 
  
<span data-ttu-id="9c417-136">受信者リストが大きすぎてメモリに収まらない場合、クライアントは [IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出して、リストのサブセットを処理できます。</span><span class="sxs-lookup"><span data-stu-id="9c417-136">If a recipient list is too large to fit in memory, clients can call the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to work with a subset of the list.</span></span> <span data-ttu-id="9c417-137">この状況では、クライアントはアドレス帳の一般的なダイアログ ボックスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c417-137">Clients should not use the address book common dialog boxes in this situation.</span></span> 
  
<span data-ttu-id="9c417-138">**ADRENTRY** 構造体にメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c417-138">For more information about how to allocate memory for **ADRENTRY** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c417-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c417-139">See also</span></span>

- [<span data-ttu-id="9c417-140">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="9c417-140">ADRENTRY</span></span>](adrentry.md)  
- [<span data-ttu-id="9c417-141">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="9c417-141">CbNewADRLIST</span></span>](cbnewadrlist.md) 
- [<span data-ttu-id="9c417-142">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="9c417-142">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md) 
- [<span data-ttu-id="9c417-143">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9c417-143">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="9c417-144">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9c417-144">MAPI Structures</span></span>](mapi-structures.md)

