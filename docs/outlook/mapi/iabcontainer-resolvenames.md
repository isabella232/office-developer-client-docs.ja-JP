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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ed87a2a6e3232cec492da6be032cf54cd66c3772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800341"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="ae410-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="ae410-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="ae410-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae410-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae410-105">1 つまたは複数の受信者のエントリの名前解決を実行します。</span><span class="sxs-lookup"><span data-stu-id="ae410-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="ae410-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ae410-106">Parameters</span></span>

 <span data-ttu-id="ae410-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ae410-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="ae410-108">[in]プロバイダーによって返された[ADRLIST](adrlist.md)構造体に含まれるプロパティを記述するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae410-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="ae410-109">プロバイダーの既定のプロパティのセットを要求するには、 _lpPropTagArray_パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="ae410-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="ae410-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae410-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ae410-111">[in]返される文字列内のテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ae410-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="ae410-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ae410-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ae410-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="ae410-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="ae410-114">正確なプロキシ アドレスの一致のみが検索されます。部分的な一致は無視されます。</span><span class="sxs-lookup"><span data-stu-id="ae410-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="ae410-115">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="ae410-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ae410-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ae410-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ae410-117">名前解決を実行するのには、オフライン アドレス帳のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae410-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="ae410-118">たとえば、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを有効にするのにこのフラグを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ae410-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ae410-119">このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="ae410-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="ae410-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ae410-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ae410-121">Unicode 形式では、返される文字列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ae410-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="ae410-122">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ae410-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ae410-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="ae410-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="ae410-124">[で [チェック アウト]入力、解決するのには受信者のリストを格納する**ADRLIST**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae410-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="ae410-125">出力では、解決された名前を格納する**ADRLIST**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae410-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="ae410-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="ae410-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="ae410-127">[で [チェック アウト]フラグの配列へのポインター、 _lpAdrList_のパラメーターに[ADRENTRY](adrentry.md)構造体に対応する各フラグを提供する、受信者の名前解決操作のステータス。</span><span class="sxs-lookup"><span data-stu-id="ae410-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="ae410-128">_LpAdrList_内のエントリと同じ順序では、 _lpFlagList_パラメーター内のフラグです。</span><span class="sxs-lookup"><span data-stu-id="ae410-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="ae410-129">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ae410-129">The following flags can be set:</span></span>
    
<span data-ttu-id="ae410-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="ae410-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="ae410-131">対応する受信者が解決されていませんが、エントリの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="ae410-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="ae410-132">他のコンテナーは、この受信者を解決するのにはいけません。</span><span class="sxs-lookup"><span data-stu-id="ae410-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="ae410-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="ae410-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="ae410-134">エントリの一意の識別子に対応する受信者を解決されています。</span><span class="sxs-lookup"><span data-stu-id="ae410-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="ae410-135">他のコンテナーは、この受信者を解決するのにはいけません。</span><span class="sxs-lookup"><span data-stu-id="ae410-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="ae410-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="ae410-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="ae410-137">対応するエントリが解決されていません。</span><span class="sxs-lookup"><span data-stu-id="ae410-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="ae410-138">他のコンテナーは、この受信者を解決するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ae410-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae410-139">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ae410-139">Return value</span></span>

<span data-ttu-id="ae410-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae410-140">S_OK</span></span> 
  
> <span data-ttu-id="ae410-141">名前解決の処理が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="ae410-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="ae410-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ae410-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ae410-143">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ae410-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ae410-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ae410-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ae410-145">アドレス帳プロバイダーは、このメソッドを使用して一括名前解決をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ae410-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae410-146">備考</span><span class="sxs-lookup"><span data-stu-id="ae410-146">Remarks</span></span>

<span data-ttu-id="ae410-147">**ResolveNames**メソッドは、このアドレス帳コンテナー内の受信者に、 _lpAdrList_パラメーター内のエントリの配列からの未解決の受信者に一致しようとします。</span><span class="sxs-lookup"><span data-stu-id="ae410-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="ae410-148">未解決の受信者には、通常、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティのみと可能性のあるいくつかの他のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="ae410-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="ae410-149">未解決の受信者にプロパティがない、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) と MAPI_UNRESOLVED に、 _lpFlagList_パラメーターに対応する、フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae410-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="ae410-150">逆に、解決済みの受信者は常に少なくとも**PR_ENTRYID**プロパティと**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))、 **PR_DISPLAY_NAME**、 **PR_ADDRTYPE** ([などの他のいくつかのプロパティPidTagAddressType](pidtagaddresstype-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="ae410-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="ae410-151">名前解決は、クライアントが、 [IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを呼び出すと通常起動します。</span><span class="sxs-lookup"><span data-stu-id="ae410-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="ae410-152">Outlook MAPI は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) のプロパティで指定されたアドレス帳検索パスに含まれるそれぞれのアドレス帳コンテナーの**ResolveNames**メソッドを呼び出すことによって応答します。</span><span class="sxs-lookup"><span data-stu-id="ae410-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="ae410-153">_LpAdrList_パラメーター内のエントリには、受信者検索パスの前のエントリが表示されるための MAPI が既に呼び出されて**ResolveNames**コンテナーにいるので、既に解決にはが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae410-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="ae410-154">各コンテナーは、そのエントリのいずれかの表示名と、受信者の表示名を照合することによって、未解決のエントリを解決するしようとします。</span><span class="sxs-lookup"><span data-stu-id="ae410-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="ae410-155">一意の一致が見つかると、 **ResolveNames** **PR_ENTRYID**プロパティと送信の**ADRLIST**構造体の対応するエントリを_lpPropTagArray_パラメーターに含まれるその他のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae410-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="ae410-156">**ResolveNames** MAPI_RESOLVED に_lpFlagList_パラメーターにエントリを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae410-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="ae410-157">**PR_ENTRYID**プロパティに格納されているエントリの識別子は、短期的または長期的にできます。</span><span class="sxs-lookup"><span data-stu-id="ae410-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="ae410-158">結局のところ、検索で使用するコンテナーのパスが試行されると名前解決プロセス、MAPI ダイアログが開き、可能であれば、残りの競合を解決するのにユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="ae410-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="ae410-159">クライアントでは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドの呼び出しで返された**ADRLIST**構造体を使用することも。</span><span class="sxs-lookup"><span data-stu-id="ae410-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ae410-160">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ae410-160">Notes to implementers</span></span>

<span data-ttu-id="ae410-161">**ResolveNames**メソッドを使用して名前解決をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ae410-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="ae410-162">代わりに、またはさらは、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) のプロパティの制限をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="ae410-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="ae410-163">名前解決のための**PR_ANR**の制限に依存している場合は、MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="ae410-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="ae410-164">詳細については、[名前解決の実装](implementing-name-resolution.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae410-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="ae410-165">コンテナーの受信者のいずれかの受信者に一致しない場合は、MAPI_UNRESOLVED、 _lpFlagList_パラメーターで、受信者のフラグのエントリを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae410-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="ae410-166">受信者には、複数の受信者が一致すると、そのフラグを MAPI_AMBIGUOUS に設定しの**ADRENTRY**の構造を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="ae410-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="ae410-167">MAPI には、メッセージの受信者のリストに含まれる受信者の特定のプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="ae410-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="ae410-168">名前解決プロセスの一環としての**ADRENTRY**構造体に含まれてまたは[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)と[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)メソッドの呼び出しを要求したときに MAPI を待機できます。</span><span class="sxs-lookup"><span data-stu-id="ae410-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="ae410-169">これらの余分な呼び出しを削除および解決済みのすべての受信者の**ADRENTRY**構造体の次のプロパティを含めることによってパフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="ae410-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="ae410-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="ae410-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="ae410-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="ae410-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="ae410-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="ae410-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="ae410-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="ae410-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="ae410-174">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae410-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ae410-175">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae410-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="ae410-176">**PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae410-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="ae410-177">_LpPropTagArray_パラメーターのプロパティの一部が表示されません-通常コンテナーのエントリがサポートされていないためプロパティとそれらに含まれない**ADRLIST**構造内の受信者の**ADRENTRY**のメンバー。PT_ERROR に使用できない各プロパティのプロパティの種類を設定します。</span><span class="sxs-lookup"><span data-stu-id="ae410-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="ae410-178">解決済みの受信者の**ADRENTRY**構造体からプロパティを削除されません。</span><span class="sxs-lookup"><span data-stu-id="ae410-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="ae410-179">必要があります交換ではなく、 **ADRENTRY**構造体を変更する場合、は、最初に関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) 、元の**ADRENTRY**構造体を解放し、交換用の[と**ADRENTRY**の構造体を割り当てるMAPIAllocateBuffer](mapiallocatebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="ae410-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae410-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae410-180">See also</span></span>



[<span data-ttu-id="ae410-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ae410-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="ae410-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ae410-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ae410-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="ae410-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="ae410-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="ae410-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="ae410-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="ae410-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="ae410-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ae410-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="ae410-187">PidTagAnr の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ae410-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="ae410-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ae410-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="ae410-189">これにより: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ae410-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

