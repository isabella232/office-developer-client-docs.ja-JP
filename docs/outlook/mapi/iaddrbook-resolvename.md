---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408132"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="fa9b2-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="fa9b2-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="fa9b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa9b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa9b2-105">名前解決を実行し、受信者リストの受信者にエントリ識別子を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="fa9b2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa9b2-106">Parameters</span></span>

 <span data-ttu-id="fa9b2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fa9b2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="fa9b2-108">[in]ユーザーにあいまい性の解決を求めるダイアログ ボックスの親ウィンドウへのハンドルを指定すると表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="fa9b2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa9b2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fa9b2-110">[in]解決プロセスのさまざまな側面を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="fa9b2-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-111">The following flags can be set:</span></span>
    
<span data-ttu-id="fa9b2-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="fa9b2-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="fa9b2-113">_lpszNewEntryTitle が_ UNICODE 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="fa9b2-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fa9b2-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="fa9b2-115">名前解決を実行するには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="fa9b2-116">たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="fa9b2-117">このフラグは、アドレス帳プロバイダー Exchangeサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="fa9b2-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fa9b2-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="fa9b2-119">ユーザーに追加の名前解決情報を求めるダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="fa9b2-120">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="fa9b2-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fa9b2-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fa9b2-122">アドレス一覧で返されるプロパティは、アドレス一覧ではなく、PT_UNICODE型PT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="fa9b2-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="fa9b2-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="fa9b2-124">[in]ユーザーに受信者の入力を求めるダイアログ ボックス内のコントロールのタイトルのテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="fa9b2-125">タイトルは受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="fa9b2-126">_lpszNewEntryTitle パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="fa9b2-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="fa9b2-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="fa9b2-128">[インアウト]解決する受信者名の一覧を含む [ADRLIST](adrlist.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="fa9b2-129">この **ADRLIST 構造** は [、IAddrBook::Address メソッドによって作成](iaddrbook-address.md) できます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa9b2-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa9b2-130">Return value</span></span>

<span data-ttu-id="fa9b2-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa9b2-131">S_OK</span></span> 
  
> <span data-ttu-id="fa9b2-132">名前解決プロセスが成功しました。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="fa9b2-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="fa9b2-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="fa9b2-134">_lpAdrList_ パラメーター内の少なくとも 1 つの受信者が、アドレス帳内の複数のエントリと一致しました。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="fa9b2-135">通常、この値は、MAPI_DIALOGフラグが設定されている場合に返され、ダイアログ ボックスの表示は禁止されます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="fa9b2-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa9b2-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fa9b2-137">_lpAdrList_ パラメーター内の少なくとも 1 つの受信者を解決できません。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="fa9b2-138">通常、この値は、MAPI_DIALOGフラグが設定されている場合に返され、ダイアログ ボックスの表示は禁止されます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa9b2-139">注釈</span><span class="sxs-lookup"><span data-stu-id="fa9b2-139">Remarks</span></span>

<span data-ttu-id="fa9b2-140">クライアントとサービス プロバイダーは **ResolveName メソッドを呼び出** して、名前解決プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="fa9b2-141">未解決のエントリは、まだエントリ識別子またはプロパティ [(PidTagEntryId)](pidtagentryid-canonical-property.md)プロパティ **PR_ENTRYIDエントリです**。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="fa9b2-142">**ResolveName** は  _、lpAdrList_ パラメーターで渡されたアドレス一覧内の未解決のエントリごとに、次のプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="fa9b2-143">受信者のアドレスの種類が SMTP アドレス _(displayname_ @  _domain.top-level-domain)_ の形式に準拠している場合 **、ResolveName** は一時エントリ識別子を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="fa9b2-144">ResolveName は、PR_AB_SEARCH_PATH **(** [PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティ内の各コンテナーについて [、IABContainer::ResolveNames メソッドを呼び出](iabcontainer-resolvenames.md)します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="fa9b2-145">**ResolveNames は** 、未解決の各受信者の表示名を、そのエントリの 1 つに属する表示名と一致します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="fa9b2-146">コンテナーが **ResolveNames** をサポートしていない **場合、ResolveName** は、プロパティ制限 ([PidTagAnr](pidtaganr-canonical-property.md)) PR_ANR を使用してコンテナーのコンテンツ **テーブル** を制限します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="fa9b2-147">この制限により、コンテナーは一致する受信者を検索する "最適な推測" タイプの検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="fa9b2-148">すべてのコンテナーは、プロパティ **の制限** PR_ANR必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="fa9b2-149">コンテナーが複数の名前に一致する受信者を返す場合 **、ResolveName** は MAPI_DIALOG フラグが設定されている場合にダイアログ ボックスを表示し、ユーザーが正しい名前を選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="fa9b2-150">PR_AB_SEARCH_PATH プロパティ **内のすべてのコンテナーが** 呼び出され、一致が見つからない場合、受信者は未解決のままです。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="fa9b2-151">1 つ以上の受信者が未解決の場合 **、ResolveName** は新しい受信者MAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="fa9b2-152">1 つ以上の受信者が、ダイアログ ボックスで解決できないあいまいな解決策を持っていた場合、または MAPI_DIALOG フラグが設定されていない場合 **、ResolveName** は MAPI_E_AMBIGUOUS_RECIP を返します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="fa9b2-153">一部の受信者があいまいで解決できない場合 **、ResolveName** はどちらのエラー値も返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="fa9b2-154">名前を解決できない場合、クライアントは、特別な形式のアドレスとエントリ識別子を持つ 1 回のアドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="fa9b2-155">1 回きりエントリ識別子の形式の詳細については [、「One-Off Entry IDENTIFIERs」を参照してください](one-off-entry-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="fa9b2-156">1 回のアドレスの形式の詳細については [、「One-Off Addresses 」を参照してください](one-off-addresses.md)。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="fa9b2-157">MAPI では **、ADRLIST** の Unicode 文字文字列と ResolveName への新しいエントリ タイトル パラメーター **がサポートされています**。このフラグを設定MAPI_UNICODE、次のプロパティは [ADRENTRY](adrentry.md) 構造体の型PT_UNICODE返されます。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="fa9b2-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fa9b2-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="fa9b2-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fa9b2-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="fa9b2-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fa9b2-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="fa9b2-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fa9b2-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="fa9b2-162">ただし **、PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) プロパティは、常に型として返PT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fa9b2-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fa9b2-163">MFCMAPI reference</span></span>

<span data-ttu-id="fa9b2-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fa9b2-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fa9b2-165">**File**</span></span>|<span data-ttu-id="fa9b2-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="fa9b2-166">**Function**</span></span>|<span data-ttu-id="fa9b2-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="fa9b2-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa9b2-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fa9b2-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fa9b2-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="fa9b2-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="fa9b2-170">MFCMAPI は **ResolveName** メソッドを使用して、メッセージに追加する前に 1 回のアドレスを解決します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="fa9b2-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fa9b2-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fa9b2-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="fa9b2-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="fa9b2-173">MFCMAPI は **ResolveName メソッドを使用** して、表示名でアドレス帳エントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="fa9b2-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa9b2-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa9b2-174">See also</span></span>



[<span data-ttu-id="fa9b2-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="fa9b2-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="fa9b2-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="fa9b2-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="fa9b2-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="fa9b2-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="fa9b2-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fa9b2-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="fa9b2-179">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fa9b2-179">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

