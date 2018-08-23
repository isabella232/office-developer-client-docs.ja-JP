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
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800376"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="a6086-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="a6086-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="a6086-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6086-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6086-105">宛先リスト内の受信者にエントリの識別子を割り当て、名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6086-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="a6086-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6086-106">Parameters</span></span>

 <span data-ttu-id="a6086-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a6086-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a6086-108">[in]、表示されるダイアログ ボックスの親ウィンドウへのハンドルのあいまいさを解決するのにはユーザーに確認する、指定した場合。</span><span class="sxs-lookup"><span data-stu-id="a6086-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="a6086-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6086-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a6086-110">[in]解決プロセスのさまざまな側面を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a6086-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="a6086-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a6086-111">The following flags can be set:</span></span>
    
<span data-ttu-id="a6086-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="a6086-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="a6086-113">その_lpszNewEntryTitle_が UNICODE 文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="a6086-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="a6086-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="a6086-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="a6086-115">名前解決を実行するのにには、オフライン アドレス帳のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6086-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="a6086-116">たとえば、このフラグを使用すると、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを許可します。</span><span class="sxs-lookup"><span data-stu-id="a6086-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="a6086-117">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="a6086-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="a6086-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a6086-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a6086-119">その他の名前解決情報をユーザーに確認するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6086-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="a6086-120">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a6086-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="a6086-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6086-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a6086-122">PT_STRING8 の代わりに PT_UNICODE の種類のアドレス] ボックスの一覧で返されるプロパティがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="a6086-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="a6086-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="a6086-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="a6086-124">[in]受信者を入力するように求めるダイアログ ボックスで、コントロールのタイトルのテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6086-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="a6086-125">タイトルは、受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a6086-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="a6086-126">_LpszNewEntryTitle_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="a6086-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a6086-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="a6086-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="a6086-128">[out]解決するのには受信者の名前のリストを格納する[ADRLIST](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6086-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="a6086-129">[IAddrBook::Address](iaddrbook-address.md)メソッドでは、この**ADRLIST**の構造体を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6086-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6086-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a6086-130">Return value</span></span>

<span data-ttu-id="a6086-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6086-131">S_OK</span></span> 
  
> <span data-ttu-id="a6086-132">名前解決の処理に成功しました。</span><span class="sxs-lookup"><span data-stu-id="a6086-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="a6086-133">これらが同じ</span><span class="sxs-lookup"><span data-stu-id="a6086-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="a6086-134">_LpAdrList_パラメーターで 1 つ以上の受信者には、アドレス帳に複数のエントリが一致します。</span><span class="sxs-lookup"><span data-stu-id="a6086-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="a6086-135">通常、MAPI_DIALOG フラグを設定すると、ダイアログ ボックスの表示を禁止する場合にこの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a6086-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="a6086-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a6086-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a6086-137">_LpAdrList_パラメーターで 1 つ以上の受信者を解決できません。</span><span class="sxs-lookup"><span data-stu-id="a6086-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="a6086-138">通常、MAPI_DIALOG フラグを設定すると、ダイアログ ボックスの表示を禁止する場合にこの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a6086-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a6086-139">注釈</span><span class="sxs-lookup"><span data-stu-id="a6086-139">Remarks</span></span>

<span data-ttu-id="a6086-140">クライアントとサービス ・ プロバイダーは、名前解決プロセスを開始する**ResolveName**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6086-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="a6086-141">未解決のエントリは、エントリがないまだエントリの識別子またはプロパティの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) です。</span><span class="sxs-lookup"><span data-stu-id="a6086-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="a6086-142">**ResolveName**は、 _lpAdrList_パラメーターで渡されたアドレス一覧に未解決のエントリごとに次のプロセスを通過します。</span><span class="sxs-lookup"><span data-stu-id="a6086-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="a6086-143">受信者のアドレスの種類が SMTP アドレスの形式に準拠している場合 (_表示名_@ _domain.top ・ レベル ・ ドメイン_)、 **ResolveName**はそれに 1 回限りのエントリの識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a6086-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="a6086-144">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) のプロパティ内の各コンテナーには、 **ResolveName**は、 [IABContainer::ResolveNames](iabcontainer-resolvenames.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6086-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="a6086-145">**ResolveNames**が表示名のエントリのいずれかに属しますが、未解決の各受信者の表示名を一致させようとするとします。</span><span class="sxs-lookup"><span data-stu-id="a6086-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="a6086-146">コンテナーが**ResolveNames**をサポートしていない場合、 **ResolveName**は**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を使用してコンテナーの内容のテーブルを制限します。</span><span class="sxs-lookup"><span data-stu-id="a6086-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="a6086-147">この制限には、「最適な推測」一致する受信者を検索する検索の種類を実行するコンテナーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a6086-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="a6086-148">すべてのコンテナーには、 **PR_ANR**プロパティ制限をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6086-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="a6086-149">コンテナーに複数の名前に一致する受信者が返されるとき**ResolveName**は、MAPI_DIALOG フラグが設定されて、ユーザーが正しい名前を選択できるようにする場合にダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="a6086-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="a6086-150">すべての**PR_AB_SEARCH_PATH**プロパティのコンテナーが呼び出された場合は、一致するものが見つかりませんでした、受信者は未解決のままになります。</span><span class="sxs-lookup"><span data-stu-id="a6086-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="a6086-151">1 つまたは複数の受信者が解決できない、 **ResolveName**は MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="a6086-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="a6086-152">**ResolveName**は] ダイアログ ボックスでは、解決できませんでしたが、あいまいな解像度を 1 つまたは複数の宛先があった場合、MAPI_DIALOG フラグが設定されていないために、これらが同じを返します。</span><span class="sxs-lookup"><span data-stu-id="a6086-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="a6086-153">一部の受信者があいまいで、いくつかを解決することはできません、 **ResolveName**はいずれかのエラー値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a6086-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="a6086-154">名前を解決できない場合、クライアントは特別な形式のアドレスとエントリの識別子を持つ一時アドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6086-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="a6086-155">一時エントリ id の形式の詳細については、 [1 回限りのエントリ Id](one-off-entry-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6086-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="a6086-156">一時アドレスの形式の詳細については、[一時アドレス](one-off-addresses.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6086-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="a6086-157">MAPI の**ADRLIST**新しいエントリのタイトル**ResolveName**; 文字の Unicode 文字列をサポートしていますMAPI_UNICODE フラグを設定する場合は、 [ADRENTRY](adrentry.md)構造体の PT_UNICODE の種類として、次のプロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="a6086-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="a6086-158">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6086-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="a6086-159">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6086-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="a6086-160">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6086-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="a6086-161">**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a6086-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="a6086-162">ただし、PT_STRING8 を型としては、 **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) のプロパティは常に返されます。</span><span class="sxs-lookup"><span data-stu-id="a6086-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6086-163">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="a6086-163">MFCMAPI reference</span></span>

<span data-ttu-id="a6086-164">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a6086-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6086-165">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="a6086-165">**File**</span></span>|<span data-ttu-id="a6086-166">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="a6086-166">**Function**</span></span>|<span data-ttu-id="a6086-167">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="a6086-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6086-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a6086-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a6086-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="a6086-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="a6086-170">MFCMAPI では、メッセージに追加する前に 1 回限りのアドレスを解決するのには、 **ResolveName**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6086-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="a6086-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a6086-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a6086-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="a6086-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="a6086-173">MFCMAPI では、 **ResolveName**メソッドを使用して、表示名、アドレス帳エントリを検索します。</span><span class="sxs-lookup"><span data-stu-id="a6086-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6086-174">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6086-174">See also</span></span>



[<span data-ttu-id="a6086-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="a6086-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="a6086-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="a6086-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="a6086-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="a6086-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="a6086-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6086-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="a6086-179">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a6086-179">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

