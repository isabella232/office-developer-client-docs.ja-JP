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
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="75dd4-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="75dd4-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="75dd4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75dd4-105">1つまたは複数の受信者エントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="75dd4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="75dd4-106">Parameters</span></span>

 <span data-ttu-id="75dd4-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="75dd4-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="75dd4-108">順番プロバイダーによって返される[adrlist](adrlist.md)構造に含まれるプロパティを説明するプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="75dd4-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="75dd4-109">プロバイダーの既定のプロパティセットを要求するには、 _lpPropTagArray_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="75dd4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75dd4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="75dd4-111">順番返される文字列内のテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="75dd4-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="75dd4-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-112">The following flags can be set:</span></span>
    
<span data-ttu-id="75dd4-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="75dd4-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="75dd4-114">完全に一致するプロキシアドレスのみが検索されます。部分一致は無視されます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="75dd4-115">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="75dd4-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="75dd4-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="75dd4-117">名前解決を実行するために使用されるのは、オフラインアドレス帳のみです。</span><span class="sxs-lookup"><span data-stu-id="75dd4-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="75dd4-118">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="75dd4-119">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="75dd4-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75dd4-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="75dd4-121">返される文字列プロパティは、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="75dd4-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="75dd4-122">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="75dd4-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="75dd4-123">_lpadrlist_</span><span class="sxs-lookup"><span data-stu-id="75dd4-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="75dd4-124">[入力]入力時に、解決される受信者のリストを含む**adrlist**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="75dd4-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="75dd4-125">出力時に、解決された名前を含む**adrlist**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="75dd4-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="75dd4-126">_lpflaglist_</span><span class="sxs-lookup"><span data-stu-id="75dd4-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="75dd4-127">[入力]フラグの配列へのポインター。 _lpadrlist_パラメーターの[adrentry](adrentry.md)構造に対応する各フラグは、受信者の名前解決操作の状態を提供します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="75dd4-128">_lpflaglist_パラメーターのフラグは、 _lpadrlist_のエントリと同じ順序になっています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="75dd4-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-129">The following flags can be set:</span></span>
    
<span data-ttu-id="75dd4-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="75dd4-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="75dd4-131">対応する受信者は解決されましたが、一意のエントリ識別子は解決されていません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="75dd4-132">他のコンテナーは、この受信者の解決を試みてはなりません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="75dd4-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="75dd4-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="75dd4-134">対応する受信者が一意のエントリ識別子に解決されました。</span><span class="sxs-lookup"><span data-stu-id="75dd4-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="75dd4-135">他のコンテナーは、この受信者の解決を試みてはなりません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="75dd4-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="75dd4-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="75dd4-137">対応するエントリは解決されていません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="75dd4-138">他のコンテナーは、この受信者の解決を試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75dd4-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="75dd4-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="75dd4-139">Return value</span></span>

<span data-ttu-id="75dd4-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="75dd4-140">S_OK</span></span> 
  
> <span data-ttu-id="75dd4-141">名前解決プロセスが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="75dd4-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="75dd4-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="75dd4-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="75dd4-143">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="75dd4-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="75dd4-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="75dd4-145">アドレス帳プロバイダーは、このメソッドを使用したバルク名解決をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75dd4-146">注釈</span><span class="sxs-lookup"><span data-stu-id="75dd4-146">Remarks</span></span>

<span data-ttu-id="75dd4-147">**ResolveNames**メソッドは、解決されない受信者を、 _lpadrlist_パラメーター内のエントリの配列から、このアドレス帳コンテナー内の受信者に一致させようとします。</span><span class="sxs-lookup"><span data-stu-id="75dd4-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="75dd4-148">未解決の受信者には、通常、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティだけがあり、他にもいくつかのプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="75dd4-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="75dd4-149">未解決の受信者には、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティがありません。 _lpflaglist_パラメーター内の対応するフラグは MAPI_UNRESOLVED に設定されています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="75dd4-150">反対に、解決された受信者には、少なくとも**PR_ENTRYID**プロパティと、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))、 **PR_DISPLAY_NAME**、 **PR_ADDRTYPE**などのその他のプロパティがあります ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="75dd4-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="75dd4-151">通常、クライアントが[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドを呼び出すときに、名前解決が開始されます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="75dd4-152">Outlook MAPI は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティによって指定されたアドレス帳の検索パスに含まれる各アドレス帳コンテナーの**ResolveNames**メソッドを呼び出すことによって応答します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="75dd4-153">_lpadrlist_パラメーターのエントリには、検索パスの前にエントリが表示されているため、MAPI が既に**ResolveNames**を呼び出しているコンテナーにあるため、既に解決されている受信者が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75dd4-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="75dd4-154">各コンテナーは、受信者の表示名とそのエントリの表示名を一致させることによって、未解決のエントリの解決を試みます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="75dd4-155">一意の一致が見つかった場合、 **ResolveNames**は、 **PR_ENTRYID**プロパティと、 _lpPropTagArray_パラメーターに含まれるその他のプロパティを、出力する**adrlist**構造体の対応するエントリに追加します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="75dd4-156">**ResolveNames**は、 _lpflaglist_パラメーターのエントリを MAPI_RESOLVED に設定します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="75dd4-157">**PR_ENTRYID**プロパティに格納されているエントリ識別子は、短期的または長期間の場合があります。</span><span class="sxs-lookup"><span data-stu-id="75dd4-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="75dd4-158">検索パス内のすべてのコンテナーが名前解決プロセスを試行した後、MAPI によっては、可能であれば、残りの競合を解決するためにユーザーに支援を求めるダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="75dd4-159">クライアントは、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドへの呼び出しで、返された**adrlist**構造を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="75dd4-160">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="75dd4-160">Notes to implementers</span></span>

<span data-ttu-id="75dd4-161">**ResolveNames**メソッドを使用して名前解決をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="75dd4-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="75dd4-162">代わりに、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を使用してサポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="75dd4-163">名前解決の**PR_ANR**制限に頼る場合は、MAPI_E_NO_SUPPORT を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="75dd4-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="75dd4-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="75dd4-165">受信者がコンテナーのどの受信者とも一致しない場合は、 _lpflaglist_パラメーターの受信者のフラグエントリを MAPI_UNRESOLVED に設定します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="75dd4-166">受信者が複数の受信者と一致する場合は、そのフラグを MAPI_AMBIGUOUS に設定し、 **adrentry**構造を変更しないようにします。</span><span class="sxs-lookup"><span data-stu-id="75dd4-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="75dd4-167">MAPI では、メッセージの宛先リストに含まれる受信者に特定のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="75dd4-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="75dd4-168">名前解決プロセスの一部として、これらを**adrentry**構造に含めるか、MAPI が[IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドと[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)メソッドへの呼び出しを要求するようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="75dd4-169">解決されたすべての受信者の**adrentry**構造に次のプロパティを含めることで、これらの余分な呼び出しを排除し、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="75dd4-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="75dd4-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="75dd4-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="75dd4-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="75dd4-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="75dd4-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="75dd4-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="75dd4-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="75dd4-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="75dd4-174">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="75dd4-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="75dd4-175">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="75dd4-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="75dd4-176">**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="75dd4-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="75dd4-177">_lpPropTagArray_パラメーターの一部のプロパティが使用できない場合 (通常は container エントリがプロパティをサポートしておらず、かつ、 **adrentry**構造の受信者の**adrentry**メンバーに含まれていないためです)。使用できない各プロパティのプロパティの種類を PT_ERROR に設定します。</span><span class="sxs-lookup"><span data-stu-id="75dd4-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="75dd4-178">解決された受信者の**adrentry**構造からはプロパティを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="75dd4-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="75dd4-179">**adrentry**構造を変更するのではなく、最初に元の**adrentry**構造を解放する必要がある場合は、まず、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、次のように\*\*\*\* [置き換えられた adrentry 構造をMAPIAllocateBuffer](mapiallocatebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="75dd4-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75dd4-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="75dd4-180">See also</span></span>



[<span data-ttu-id="75dd4-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="75dd4-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="75dd4-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="75dd4-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="75dd4-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="75dd4-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="75dd4-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="75dd4-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="75dd4-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="75dd4-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="75dd4-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="75dd4-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="75dd4-187">PidTagAnr 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75dd4-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="75dd4-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="75dd4-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="75dd4-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="75dd4-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

