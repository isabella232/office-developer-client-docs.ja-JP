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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339222"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="c96d3-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="c96d3-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="c96d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c96d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c96d3-105">メッセージングシステムで後で使用するために、受信者リストを準備します。</span><span class="sxs-lookup"><span data-stu-id="c96d3-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="c96d3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c96d3-106">Parameters</span></span>

 <span data-ttu-id="c96d3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c96d3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c96d3-108">順番エントリが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c96d3-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="c96d3-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c96d3-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c96d3-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c96d3-111">名前解決を実行するには、オフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="c96d3-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="c96d3-112">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c96d3-113">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c96d3-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="c96d3-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c96d3-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="c96d3-115">順番更新が必要なプロパティがある場合に、そのプロパティを示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c96d3-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="c96d3-116">_lpSPropTagArray_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="c96d3-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="c96d3-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="c96d3-118">順番受信者のリストを含む[adrlist](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c96d3-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c96d3-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c96d3-119">Return value</span></span>

<span data-ttu-id="c96d3-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c96d3-120">S_OK</span></span> 
  
> <span data-ttu-id="c96d3-121">受信者リストが正常に準備されました。</span><span class="sxs-lookup"><span data-stu-id="c96d3-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c96d3-122">解説</span><span class="sxs-lookup"><span data-stu-id="c96d3-122">Remarks</span></span>

<span data-ttu-id="c96d3-123">クライアントおよびサービスプロバイダーは、 **PrepareRecips**メソッドを呼び出して次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="c96d3-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="c96d3-124">_lpRecipList_パラメーターのすべての受信者が長期間のエントリ識別子を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c96d3-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="c96d3-125">_lpRecipList_パラメーターの各受信者の_lpSPropTagArray_パラメーターにプロパティがリストされていること、およびこれらのプロパティが受信者リストの先頭に表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c96d3-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="c96d3-126">MAPI は、各受信者の短い用語エントリ識別子を長期のエントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="c96d3-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="c96d3-127">必要に応じて、受信者の長期入力識別子が適切なアドレス帳プロバイダーから取得され、追加のプロパティが要求されます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="c96d3-128">個別の受信者エントリでは、要求されたプロパティが最初に並べ替えられ、その後にエントリに既に存在していたプロパティが続きます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="c96d3-129">_lpSPropTagArray_パラメーターで要求されたプロパティの1つ以上が、適切なアドレス帳プロバイダーによって処理されない場合は、そのプロパティの種類は PT_ERROR に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="c96d3-130">プロパティの値は、MAPI_E_NOT_FOUND に設定されるか、プロパティが使用できないより具体的な理由を示す別の値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="c96d3-131">_lpRecipList_パラメーターに含まれる各[spropvalue](spropvalue.md)構造体は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して個別に割り当てる必要があります。これにより、個別に解放することができます。</span><span class="sxs-lookup"><span data-stu-id="c96d3-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="c96d3-132">PT_ERROR の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c96d3-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c96d3-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c96d3-133">See also</span></span>



[<span data-ttu-id="c96d3-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c96d3-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c96d3-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c96d3-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c96d3-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c96d3-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="c96d3-137">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c96d3-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="c96d3-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c96d3-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c96d3-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="c96d3-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="c96d3-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c96d3-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

