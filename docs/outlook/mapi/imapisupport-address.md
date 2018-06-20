---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800722"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="60dda-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="60dda-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="60dda-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60dda-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60dda-105">共通のアドレス] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="60dda-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="60dda-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="60dda-106">Parameters</span></span>

 <span data-ttu-id="60dda-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="60dda-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="60dda-108">[で [チェック アウト]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="60dda-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="60dda-109">入力、ウィンドウ ハンドルを渡す必要が常にあります。</span><span class="sxs-lookup"><span data-stu-id="60dda-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="60dda-110">出力、DIALOG_SDI フラグは、 _lpAdrParms_パラメーターで指定された[ADRPARM](adrparm.md)構造体に設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="60dda-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="60dda-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="60dda-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="60dda-112">[で [チェック アウト]プレゼンテーションと、[アドレス] ダイアログ ボックスの動作を制御する**ADRPARM**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="60dda-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="60dda-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="60dda-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="60dda-114">[で [チェック アウト]アドレス一覧へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="60dda-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="60dda-115">入力でこのリストは、いずれかのメッセージ内の受信者の現在のリストまたは NULL の場合、このようなリストが存在しない場合。</span><span class="sxs-lookup"><span data-stu-id="60dda-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="60dda-116">出力では、 _lppAdrList_は、最新のメッセージの受信者の一覧をポイントします。</span><span class="sxs-lookup"><span data-stu-id="60dda-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60dda-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="60dda-117">Return value</span></span>

<span data-ttu-id="60dda-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="60dda-118">S_OK</span></span> 
  
> <span data-ttu-id="60dda-119">[アドレス] ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="60dda-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60dda-120">備考</span><span class="sxs-lookup"><span data-stu-id="60dda-120">Remarks</span></span>

<span data-ttu-id="60dda-121">アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::Address**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="60dda-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="60dda-122">アドレス帳プロバイダーは、メッセージの受信者の一覧を作成または**アドレス**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60dda-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="60dda-123">各受信者は、 _lppAdrList_パラメーターで指定された[ADRLIST](adrlist.md)構造体に含まれる[ADRENTRY](adrentry.md)構造体の説明です。</span><span class="sxs-lookup"><span data-stu-id="60dda-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="60dda-124">**ADRENTRY**構造体には、受信者のプロパティの値のうちの 1 つは、受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="60dda-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="60dda-125">[IMessage::ModifyRecipients](imessage-modifyrecipients.md)への呼び出しで、 _lpMods_のパラメーターとして使用するクライアントには、この**ADRLIST**の構造体を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="60dda-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="60dda-126">**ADRLIST**構造体の各受信者も解決できるを示すこと、プロパティの値のいずれかの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティは、未解決の**PR_ENTRYID**プロパティがあることを示します不足しています。</span><span class="sxs-lookup"><span data-stu-id="60dda-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="60dda-127">**PR_ENTRYID**、他は、解決の受信者には、次のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60dda-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="60dda-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="60dda-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="60dda-129">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60dda-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="60dda-130">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60dda-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="60dda-131">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="60dda-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="60dda-132">未解決の受信者には、通常、 **PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60dda-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="60dda-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="60dda-133">Notes to callers</span></span>

<span data-ttu-id="60dda-134">**ADRLIST**構造で、呼び出し元に合格するには、MAPI を表す構造体のサイズが異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="60dda-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="60dda-135">**ADRLIST**構造体のメモリを割り当てるときに、個別に各[SPropValue](spropvalue.md)構造体のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="60dda-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="60dda-136">メモリを割り当てるには、MAPI のメモリ割り当て関数、 [ABProviderInit](abproviderinit.md)関数に渡されたポインターを使用します。</span><span class="sxs-lookup"><span data-stu-id="60dda-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="60dda-137">**ADRLIST**と**ADRLIST**内の**ADRENTRY**構造体の各プロパティ値の構造体の[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用してメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="60dda-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="60dda-138">**アドレス**より大きな**ADRLIST**構造体を返す必要がある場合、または_lppAdrList_に NULL を渡した場合は、**アドレス**は元の構造体を解放し、新しい 1 つを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="60dda-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="60dda-139">**アドレス**は、 **ADRLIST**構造体に追加のプロパティ値の構造体を割り当てし、必要に応じて古いものを解放します。</span><span class="sxs-lookup"><span data-stu-id="60dda-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="60dda-140">**ADRLIST**構造体のメモリを管理する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60dda-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="60dda-141">_LpAdrParms_パラメーターに**ADRPARM**構造体に DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに返します。</span><span class="sxs-lookup"><span data-stu-id="60dda-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60dda-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="60dda-142">See also</span></span>



[<span data-ttu-id="60dda-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="60dda-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="60dda-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="60dda-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="60dda-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="60dda-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="60dda-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="60dda-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="60dda-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="60dda-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="60dda-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="60dda-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="60dda-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="60dda-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="60dda-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="60dda-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="60dda-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="60dda-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="60dda-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="60dda-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="60dda-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="60dda-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="60dda-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="60dda-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="60dda-155">PidTagAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="60dda-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="60dda-156">PidTagDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="60dda-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="60dda-157">PidTagDisplayType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="60dda-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="60dda-158">PidTagEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="60dda-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="60dda-159">PidTagRecipientType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="60dda-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="60dda-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="60dda-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="60dda-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="60dda-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="60dda-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="60dda-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="60dda-163">ADRLIST および SRowSet 構造体のメモリを管理します。</span><span class="sxs-lookup"><span data-stu-id="60dda-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

