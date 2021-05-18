---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405815"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="70f39-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="70f39-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="70f39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f39-105">1 つ以上の受信者エントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="70f39-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="70f39-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="70f39-106">Parameters</span></span>

 <span data-ttu-id="70f39-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="70f39-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="70f39-108">[in]プロバイダーによって返される[ADRLIST](adrlist.md)構造体に含まれるプロパティを記述するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="70f39-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="70f39-109">プロバイダーの既定のプロパティ セットを要求するには  _、lpPropTagArray_ パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="70f39-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="70f39-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70f39-110">_ulFlags_</span></span>
  
> <span data-ttu-id="70f39-111">[in]返される文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="70f39-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="70f39-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="70f39-112">The following flags can be set:</span></span>
    
<span data-ttu-id="70f39-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="70f39-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="70f39-114">プロキシ アドレスの完全一致だけが見つかる。部分一致は無視されます。</span><span class="sxs-lookup"><span data-stu-id="70f39-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="70f39-115">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="70f39-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="70f39-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="70f39-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="70f39-117">名前解決を実行するには、オフライン アドレス帳だけが使用されます。</span><span class="sxs-lookup"><span data-stu-id="70f39-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="70f39-118">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="70f39-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="70f39-119">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="70f39-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="70f39-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70f39-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70f39-121">返される文字列プロパティは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="70f39-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="70f39-122">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="70f39-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="70f39-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="70f39-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="70f39-124">[in, out]入力時に、解決する受信者の一覧を含む **ADRLIST** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="70f39-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="70f39-125">出力時に、解決された名前を含む **ADRLIST** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="70f39-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="70f39-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="70f39-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="70f39-127">[in, out]_lpAdrList_ パラメーター内の [ADRENTRY](adrentry.md)構造体に対応する各フラグの配列へのポインターで、受信者の名前解決操作の状態を提供します。</span><span class="sxs-lookup"><span data-stu-id="70f39-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="70f39-128">_lpFlagList パラメーターの_ フラグは _、lpAdrList_ のエントリと同じ順序です。</span><span class="sxs-lookup"><span data-stu-id="70f39-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="70f39-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="70f39-129">The following flags can be set:</span></span>
    
<span data-ttu-id="70f39-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="70f39-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="70f39-131">対応する受信者は解決されましたが、一意のエントリ識別子には解決されません。</span><span class="sxs-lookup"><span data-stu-id="70f39-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="70f39-132">他のコンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70f39-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="70f39-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="70f39-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="70f39-134">対応する受信者が一意のエントリ識別子に解決されました。</span><span class="sxs-lookup"><span data-stu-id="70f39-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="70f39-135">他のコンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70f39-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="70f39-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="70f39-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="70f39-137">対応するエントリは解決されません。</span><span class="sxs-lookup"><span data-stu-id="70f39-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="70f39-138">他のコンテナーは、この受信者の解決を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70f39-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70f39-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="70f39-139">Return value</span></span>

<span data-ttu-id="70f39-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="70f39-140">S_OK</span></span> 
  
> <span data-ttu-id="70f39-141">名前解決プロセスが成功しました。</span><span class="sxs-lookup"><span data-stu-id="70f39-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="70f39-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="70f39-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="70f39-143">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="70f39-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="70f39-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="70f39-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="70f39-145">アドレス帳プロバイダーは、このメソッドを使用して一括名前解決をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="70f39-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70f39-146">注釈</span><span class="sxs-lookup"><span data-stu-id="70f39-146">Remarks</span></span>

<span data-ttu-id="70f39-147">**ResolveNames** メソッドは _、lpAdrList_ パラメーター内のエントリの配列から、このアドレス帳コンテナー内の受信者に未解決の受信者を一致します。</span><span class="sxs-lookup"><span data-stu-id="70f39-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="70f39-148">未解決の受信者は、通常、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティのみを持ち、その他のいくつかのプロパティを持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="70f39-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="70f39-149">未解決の受信者には **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが設定されていないので  _、lpFlagList_ パラメーターの対応するフラグは MAPI_UNRESOLVED に設定されます。</span><span class="sxs-lookup"><span data-stu-id="70f39-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="70f39-150">逆に、解決された受信者には、少なくとも **PR_ENTRYID** プロパティと **、PR_EMAIL_ADDRESS** [(PidTagEmailAddress)、PR_DISPLAY_NAME、](pidtagemailaddress-canonical-property.md)および **PR_ADDRTYPE** **(** [PidTagAddressType)](pidtagaddresstype-canonical-property.md)などの他のいくつかのプロパティが常にあります。</span><span class="sxs-lookup"><span data-stu-id="70f39-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="70f39-151">名前の解決は、通常、クライアントが [IAddrBook::ResolveName メソッドを呼び出した場合に開始](iaddrbook-resolvename.md) されます。</span><span class="sxs-lookup"><span data-stu-id="70f39-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="70f39-152">OutlookMAPI は、PR_AB_SEARCH_PATH **(** [PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティで指定されたアドレス帳検索パスに含まれる各アドレス帳コンテナーの **ResolveNames** メソッドを呼び出して応答します。</span><span class="sxs-lookup"><span data-stu-id="70f39-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="70f39-153">_lpAdrList_ パラメーターのエントリには、MAPI が既に **ResolveNames** を呼び出しているコンテナー内にあるため、既に解決済みの受信者が含まれます。これは、エントリが検索パスの前に表示されるからです。</span><span class="sxs-lookup"><span data-stu-id="70f39-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="70f39-154">各コンテナーは、受信者の表示名とそのエントリの 1 つの表示名を照合して、未解決のエントリを解決します。</span><span class="sxs-lookup"><span data-stu-id="70f39-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="70f39-155">一意の一致が見つかった場合 **、ResolveNames** は _、lpPropTagArray_ パラメーターに含まれる **PR_ENTRYID** プロパティおよび他のプロパティを、送信 **ADRLIST** 構造体の対応するエントリに追加します。</span><span class="sxs-lookup"><span data-stu-id="70f39-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="70f39-156">**ResolveNames は**_、lpFlagList_ パラメーター内のエントリを次の値MAPI_RESOLVED。</span><span class="sxs-lookup"><span data-stu-id="70f39-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="70f39-157">PR_ENTRYID プロパティに格納 **されている** エントリ識別子は、短期的または長期的に指定できます。</span><span class="sxs-lookup"><span data-stu-id="70f39-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="70f39-158">検索パス内のすべてのコンテナーが名前解決プロセスを試みた後、MAPI はダイアログ ボックスを開き、可能であれば、残りの競合を解決するためのヘルプをユーザーに求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="70f39-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="70f39-159">クライアントは [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドの呼び出しで返される **ADRLIST** 構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="70f39-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="70f39-160">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="70f39-160">Notes to implementers</span></span>

<span data-ttu-id="70f39-161">**ResolveNames** メソッドで名前解決をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="70f39-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="70f39-162">代わりに、またはさらに、このプロパティをサポートするには、PR_ANR **(** [PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を使用します。</span><span class="sxs-lookup"><span data-stu-id="70f39-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="70f39-163">名前解決の制限に依存PR_ANR **場合は** 、名前を返MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="70f39-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="70f39-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="70f39-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="70f39-165">受信者がコンテナーの受信者と一致しない場合は  _、lpFlagList_ パラメーターの受信者のフラグ エントリを MAPI_UNRESOLVED に設定します。</span><span class="sxs-lookup"><span data-stu-id="70f39-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="70f39-166">受信者が複数の受信者と一致する場合は、そのフラグを [MAPI_AMBIGUOUS] に設定し **、ADRENTRY 構造を変更** しない。</span><span class="sxs-lookup"><span data-stu-id="70f39-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="70f39-167">MAPI には、メッセージの受信者リストに含まれる受信者の特定のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="70f39-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="70f39-168">名前解決プロセスの一部として **ADRENTRY** 構造に含めるか、MAPI が [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) および [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) メソッドへの呼び出しで要求するのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="70f39-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="70f39-169">解決済みのすべての受信者の **ADRENTRY** 構造に次のプロパティを含め、これらの余分な呼び出しを排除し、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="70f39-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="70f39-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="70f39-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="70f39-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="70f39-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="70f39-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="70f39-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="70f39-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="70f39-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="70f39-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70f39-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="70f39-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70f39-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="70f39-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70f39-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="70f39-177">_lpPropTagArray_ パラメーターのプロパティの一部が使用できない場合 (通常、コンテナー エントリはプロパティをサポートしていないので **、ADRLIST** 構造体の受信者の **ADRENTRY** メンバーに含まれていないため)、使用できない各プロパティのプロパティの種類を PT_ERROR に設定します。</span><span class="sxs-lookup"><span data-stu-id="70f39-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="70f39-178">解決済み受信者の **ADRENTRY** 構造からプロパティを削除しない。</span><span class="sxs-lookup"><span data-stu-id="70f39-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="70f39-179">**ADRENTRY** 構造体を変更するのではなく、置き換える必要がある場合は [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して最初に元の **ADRENTRY** 構造体を解放し、MAPIAllocateBuffer で置換 **ADRENTRY** 構造体を割り当てる必要があります。 [](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="70f39-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70f39-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="70f39-180">See also</span></span>



[<span data-ttu-id="70f39-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="70f39-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="70f39-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="70f39-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="70f39-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="70f39-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="70f39-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="70f39-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="70f39-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="70f39-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="70f39-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="70f39-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="70f39-187">PidTagAnr 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="70f39-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="70f39-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="70f39-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="70f39-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="70f39-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

