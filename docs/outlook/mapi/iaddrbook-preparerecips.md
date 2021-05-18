---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414278"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="df8bf-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="df8bf-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="df8bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df8bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df8bf-105">メッセージング システムで後で使用する受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="df8bf-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="df8bf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df8bf-106">Parameters</span></span>

 <span data-ttu-id="df8bf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df8bf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="df8bf-108">[in]エントリの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="df8bf-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="df8bf-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-109">The following flag can be set:</span></span>
    
<span data-ttu-id="df8bf-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="df8bf-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="df8bf-111">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="df8bf-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="df8bf-112">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳内のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="df8bf-113">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="df8bf-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="df8bf-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="df8bf-115">[in]更新が必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="df8bf-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="df8bf-116">_lpSPropTagArray パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="df8bf-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="df8bf-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="df8bf-118">[in]受信者の一覧 [を含む ADRLIST](adrlist.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="df8bf-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="df8bf-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="df8bf-119">Return value</span></span>

<span data-ttu-id="df8bf-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="df8bf-120">S_OK</span></span> 
  
> <span data-ttu-id="df8bf-121">受信者リストが正常に準備されました。</span><span class="sxs-lookup"><span data-stu-id="df8bf-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df8bf-122">注釈</span><span class="sxs-lookup"><span data-stu-id="df8bf-122">Remarks</span></span>

<span data-ttu-id="df8bf-123">クライアントとサービス プロバイダーは **PrepareRecips メソッドを呼び** 出して、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="df8bf-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="df8bf-124">_lpRecipList_ パラメーター内のすべての受信者に、長期的なエントリ識別子が設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8bf-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="df8bf-125">_lpRecipList_ パラメーターの各受信者に _、lpSPropTagArray_ パラメーターにリストされているプロパティが含み、これらのプロパティが受信者リストの最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="df8bf-126">MAPI は、各受信者の短期エントリ識別子を長期エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="df8bf-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="df8bf-127">必要に応じて、受信者の長期エントリ識別子が適切なアドレス帳プロバイダーから取得され、追加のプロパティが要求されます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="df8bf-128">個々の受信者エントリでは、要求されたプロパティが最初に順序付けされ、その後にエントリに既に存在していたプロパティが続きます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="df8bf-129">_lpSPropTagArray_ パラメーターで要求されたプロパティの 1 つ以上が適切なアドレス帳プロバイダーによって処理されない場合、プロパティの種類は PT_ERROR に設定されます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="df8bf-130">プロパティの値は、プロパティを使用できないMAPI_E_NOT_FOUND特定の理由を示す別の値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="df8bf-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="df8bf-131">_lpRecipList_ パラメーターに含まれる各 [SPropValue](spropvalue.md)構造体は [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当て、個別に解放できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8bf-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="df8bf-132">プロパティの詳細についてはPT_ERRORプロパティの [種類を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="df8bf-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df8bf-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="df8bf-133">See also</span></span>



[<span data-ttu-id="df8bf-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="df8bf-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="df8bf-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="df8bf-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="df8bf-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="df8bf-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="df8bf-137">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="df8bf-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="df8bf-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="df8bf-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="df8bf-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="df8bf-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="df8bf-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="df8bf-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

