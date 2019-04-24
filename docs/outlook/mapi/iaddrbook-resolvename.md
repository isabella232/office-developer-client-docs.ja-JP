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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287008"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="73d38-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="73d38-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="73d38-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73d38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73d38-105">名前解決を実行し、受信者リスト内の受信者にエントリ識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="73d38-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="73d38-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73d38-106">Parameters</span></span>

 <span data-ttu-id="73d38-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="73d38-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="73d38-108">順番ダイアログボックスの親ウィンドウへのハンドル。指定されている場合は、あいまいな解決をユーザーに求めるメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="73d38-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="73d38-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73d38-109">_ulFlags_</span></span>
  
> <span data-ttu-id="73d38-110">順番解決プロセスのさまざまな側面を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="73d38-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="73d38-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="73d38-111">The following flags can be set:</span></span>
    
<span data-ttu-id="73d38-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="73d38-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="73d38-113">_lpsznewentrytitle_が UNICODE 文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="73d38-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="73d38-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="73d38-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="73d38-115">名前解決を実行するには、オフラインアドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="73d38-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="73d38-116">たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="73d38-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="73d38-117">このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="73d38-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="73d38-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="73d38-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="73d38-119">追加の名前解決情報をユーザーに確認するダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="73d38-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="73d38-120">このフラグが設定されていない場合は、ダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="73d38-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="73d38-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="73d38-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="73d38-122">アドレス一覧で返されるプロパティが、PT_STRING8 ではなく PT_UNICODE 型であることを示します。</span><span class="sxs-lookup"><span data-stu-id="73d38-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="73d38-123">_lpsznewentrytitle_</span><span class="sxs-lookup"><span data-stu-id="73d38-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="73d38-124">順番ユーザーに受信者の入力を求めるダイアログボックス内のコントロールのタイトルを示すテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="73d38-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="73d38-125">タイトルは、受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="73d38-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="73d38-126">_lpsznewentrytitle_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="73d38-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="73d38-127">_lpadrlist_</span><span class="sxs-lookup"><span data-stu-id="73d38-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="73d38-128">[入力-出力]解決する受信者名のリストを含む[adrlist](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="73d38-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="73d38-129">この**adrlist**構造は、 [IAddrBook:: Address](iaddrbook-address.md)メソッドによって作成できます。</span><span class="sxs-lookup"><span data-stu-id="73d38-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73d38-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="73d38-130">Return value</span></span>

<span data-ttu-id="73d38-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="73d38-131">S_OK</span></span> 
  
> <span data-ttu-id="73d38-132">名前解決プロセスが正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="73d38-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="73d38-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="73d38-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="73d38-134">_lpadrlist_パラメーターの少なくとも1つの受信者が、アドレス帳の複数のエントリと一致しました。</span><span class="sxs-lookup"><span data-stu-id="73d38-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="73d38-135">通常、この値は、MAPI_DIALOG フラグが設定されているときに返され、ダイアログボックスの表示を禁止します。</span><span class="sxs-lookup"><span data-stu-id="73d38-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="73d38-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="73d38-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="73d38-137">_lpadrlist_パラメーターの少なくとも1人の受信者を解決できません。</span><span class="sxs-lookup"><span data-stu-id="73d38-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="73d38-138">通常、この値は、MAPI_DIALOG フラグが設定されているときに返され、ダイアログボックスの表示を禁止します。</span><span class="sxs-lookup"><span data-stu-id="73d38-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73d38-139">解説</span><span class="sxs-lookup"><span data-stu-id="73d38-139">Remarks</span></span>

<span data-ttu-id="73d38-140">クライアントおよびサービスプロバイダーは、 **ResolveName**メソッドを呼び出して名前解決プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="73d38-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="73d38-141">未解決のエントリとは、エントリ id または**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティをまだ持っていないエントリのことです。</span><span class="sxs-lookup"><span data-stu-id="73d38-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="73d38-142">_lpadrlist_パラメーターに渡されたアドレス一覧の未解決の各エントリに対して、 **ResolveName**は次のプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="73d38-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="73d38-143">受信者のアドレスの種類が SMTP アドレス ( _displayname_@ _ドメイン_) の形式に準拠している場合、 **ResolveName**は1回限りのエントリ識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="73d38-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="73d38-144">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティの各コンテナーに対して、 **ResolveName**は[IABContainer:: ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="73d38-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="73d38-145">**ResolveNames**は、各受信者の表示名を、そのエントリのいずれかに属する表示名に一致させようとします。</span><span class="sxs-lookup"><span data-stu-id="73d38-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="73d38-146">コンテナーが**ResolveNames**をサポートしていない場合、 **ResolveName**は、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を使用してコンテナーの contents テーブルを制限します。</span><span class="sxs-lookup"><span data-stu-id="73d38-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="73d38-147">この制限によって、コンテナーは一致する受信者を検索するために "最適な推測" の種類の検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="73d38-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="73d38-148">すべてのコンテナーは、 **PR_ANR**プロパティ制限をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="73d38-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="73d38-149">コンテナーが複数の名前に一致する受信者を返すと、MAPI_DIALOG フラグが設定されている場合、 **ResolveName**はダイアログボックスを表示し、ユーザーが正しい名前を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="73d38-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="73d38-150">**PR_AB_SEARCH_PATH**プロパティのすべてのコンテナーが呼び出され、一致が見つからない場合は、受信者は未解決のままになります。</span><span class="sxs-lookup"><span data-stu-id="73d38-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="73d38-151">1つまたは複数の受信者が未解決の場合、 **ResolveName**は MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="73d38-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="73d38-152">1つまたは複数の受信者があいまいな解決策をダイアログボックスで解決できない場合、または MAPI_DIALOG フラグが設定されていない場合、 **ResolveName**は MAPI_E_AMBIGUOUS_RECIP を返します。</span><span class="sxs-lookup"><span data-stu-id="73d38-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="73d38-153">一部の受信者があいまいで解決できない場合、 **ResolveName**はどちらかのエラー値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="73d38-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="73d38-154">名前を解決できない場合、クライアントは、特別な形式のアドレスとエントリ識別子を持つ1回限りのアドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="73d38-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="73d38-155">1回限りのエントリ識別子の形式の詳細については、「 [1 回限りのエントリ識別子](one-off-entry-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73d38-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="73d38-156">1回限りのアドレスの形式の詳細については、「[一時](one-off-addresses.md)アドレス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73d38-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="73d38-157">MAPI では、 **adrlist**の Unicode 文字列と、 **ResolveName**への新しいエントリタイトルパラメーターがサポートされています。MAPI_UNICODE フラグを設定した場合、 [adrentry](adrentry.md)構造では、次のプロパティが PT_UNICODE 型として返されます。</span><span class="sxs-lookup"><span data-stu-id="73d38-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="73d38-158">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="73d38-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="73d38-159">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="73d38-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="73d38-160">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="73d38-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="73d38-161">**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="73d38-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="73d38-162">ただし、 **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) プロパティは常に PT_STRING8 型として返されます。</span><span class="sxs-lookup"><span data-stu-id="73d38-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73d38-163">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="73d38-163">MFCMAPI reference</span></span>

<span data-ttu-id="73d38-164">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73d38-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73d38-165">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="73d38-165">**File**</span></span>|<span data-ttu-id="73d38-166">**関数**</span><span class="sxs-lookup"><span data-stu-id="73d38-166">**Function**</span></span>|<span data-ttu-id="73d38-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="73d38-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73d38-168">MAPIABFunctions</span><span class="sxs-lookup"><span data-stu-id="73d38-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="73d38-169">addoneoffaddress</span><span class="sxs-lookup"><span data-stu-id="73d38-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="73d38-170">mfcmapi は、メッセージに追加する前に、 **ResolveName**メソッドを使用して、1回限りのアドレスを解決します。</span><span class="sxs-lookup"><span data-stu-id="73d38-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="73d38-171">MAPIABFunctions</span><span class="sxs-lookup"><span data-stu-id="73d38-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="73d38-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="73d38-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="73d38-173">mfcmapi は、 **ResolveName**メソッドを使用して、アドレス帳のエントリを表示名で検索します。</span><span class="sxs-lookup"><span data-stu-id="73d38-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73d38-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="73d38-174">See also</span></span>



[<span data-ttu-id="73d38-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="73d38-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="73d38-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="73d38-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="73d38-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="73d38-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="73d38-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="73d38-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="73d38-179">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="73d38-179">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

