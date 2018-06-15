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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fe3e098b2b70e77bd0c536002a4724810261bff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800405"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="caeb8-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="caeb8-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="caeb8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="caeb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="caeb8-105">メッセージング システムによって後で使用できる受信者のリストを準備します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="caeb8-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="caeb8-106">Parameters</span></span>

 <span data-ttu-id="caeb8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="caeb8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="caeb8-108">[in]エントリを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="caeb8-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="caeb8-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="caeb8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="caeb8-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="caeb8-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="caeb8-111">名前解決を実行するのにには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="caeb8-112">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開くと、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="caeb8-113">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="caeb8-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="caeb8-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="caeb8-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="caeb8-115">[in]更新する必要が存在する場合、プロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="caeb8-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="caeb8-116">_LpSPropTagArray_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="caeb8-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="caeb8-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="caeb8-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="caeb8-118">[in]受信者のリストを格納する[ADRLIST](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="caeb8-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="caeb8-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="caeb8-119">Return value</span></span>

<span data-ttu-id="caeb8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="caeb8-120">S_OK</span></span> 
  
> <span data-ttu-id="caeb8-121">宛先リストの準備ができました。</span><span class="sxs-lookup"><span data-stu-id="caeb8-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caeb8-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="caeb8-122">Remarks</span></span>

<span data-ttu-id="caeb8-123">クライアントとサービス ・ プロバイダーは、以下を実行する**PrepareRecips**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="caeb8-124">_LpRecipList_パラメーター内のすべての受信者は、長期的なエントリの識別子であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="caeb8-125">_LpRecipList_パラメーターでは、各受信者が、 _lpSPropTagArray_パラメーターに表示されるプロパティを持っていると、受信者の一覧の先頭にこれらのプロパティが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="caeb8-126">MAPI では、長期のエントリ id を各受信者の短期的なエントリの識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="caeb8-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="caeb8-127">必要に応じて、適切なアドレス帳プロバイダーから受信者の長期のエントリ id を取得して、追加プロパティが要求されました。</span><span class="sxs-lookup"><span data-stu-id="caeb8-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="caeb8-128">個々 の受信者エントリ、要求されたプロパティの順序は最初に、後に既にエントリが存在していたすべてのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="caeb8-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="caeb8-129">_LpSPropTagArray_パラメーターで要求されたプロパティのいずれかが適切なアドレス帳プロバイダーによって処理されない場合、そのプロパティの型が PT_ERROR に設定されます。</span><span class="sxs-lookup"><span data-stu-id="caeb8-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="caeb8-130">プロパティ値は MAPI_E_NOT_FOUND または具体的な理由がなぜ [のプロパティは利用できませんが、別の値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="caeb8-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="caeb8-131">_LpRecipList_パラメーターに含まれる個々 の[SPropValue](spropvalue.md)構造体を個別に解放するために[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="caeb8-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="caeb8-132">PT_ERROR 詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="caeb8-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="caeb8-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="caeb8-133">See also</span></span>



[<span data-ttu-id="caeb8-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="caeb8-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="caeb8-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="caeb8-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="caeb8-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="caeb8-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="caeb8-137">PidTagEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="caeb8-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="caeb8-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="caeb8-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="caeb8-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="caeb8-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="caeb8-140">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="caeb8-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

