---
title: imapisupportaddress
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407320"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="3e1ed-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="3e1ed-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="3e1ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e1ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e1ed-105">[共通のアドレス] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="3e1ed-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e1ed-106">Parameters</span></span>

 <span data-ttu-id="3e1ed-107">_l出 uiparam_</span><span class="sxs-lookup"><span data-stu-id="3e1ed-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="3e1ed-108">[入力]ダイアログボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="3e1ed-109">入力時には、ウィンドウハンドルを常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="3e1ed-110">出力時に、DIALOG_SDI フラグが_lpadrparms_パラメーターで示される[ADRPARM](adrparm.md)構造で設定されている場合は、モードレスダイアログボックスのウィンドウハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="3e1ed-111">_lpadrparms_</span><span class="sxs-lookup"><span data-stu-id="3e1ed-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="3e1ed-112">[入力][アドレス] ダイアログボックスの表示と動作を制御する**ADRPARM**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="3e1ed-113">_lppadrlist_</span><span class="sxs-lookup"><span data-stu-id="3e1ed-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="3e1ed-114">[入力]アドレス一覧へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="3e1ed-115">入力時に、このリストは、メッセージ内の受信者の現在のリストまたは NULL (リストが存在しない場合) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="3e1ed-116">出力では、 _lppadrlist_は、更新されたメッセージ受信者のリストを指します。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e1ed-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e1ed-117">Return value</span></span>

<span data-ttu-id="3e1ed-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e1ed-118">S_OK</span></span> 
  
> <span data-ttu-id="3e1ed-119">[アドレス] ダイアログボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e1ed-120">注釈</span><span class="sxs-lookup"><span data-stu-id="3e1ed-120">Remarks</span></span>

<span data-ttu-id="3e1ed-121">**imapisupport:: address**メソッドは、アドレス帳プロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="3e1ed-122">アドレス帳プロバイダーの呼び出し**アドレス**。メッセージの受信者の一覧を作成または更新します。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="3e1ed-123">各受信者は[adrentry](adrentry.md)構造で記述されており、 _lppadrlist_パラメーターで示される[adrentry](adrlist.md)構造体に含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="3e1ed-124">**adrentry**構造には、受信者のプロパティ値の配列、1つは受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="3e1ed-125">この**adrlist**構造は、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)の呼び出しで_lpMods_パラメーターとして使用するために、クライアントに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="3e1ed-126">**adrlist**構造内の各受信者は解決できます。これは、そのプロパティ値のいずれかが**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティであるか、または未解決であることを示します。これは、 **PR_ENTRYID**プロパティがれ.</span><span class="sxs-lookup"><span data-stu-id="3e1ed-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="3e1ed-127">**PR_ENTRYID**に加えて、解決された受信者には次のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="3e1ed-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="3e1ed-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="3e1ed-129">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e1ed-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="3e1ed-130">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e1ed-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="3e1ed-131">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e1ed-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="3e1ed-132">未解決の受信者には、通常、 **PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e1ed-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3e1ed-133">Notes to callers</span></span>

<span data-ttu-id="3e1ed-134">発信者が渡す**adrlist**構造は、MAPI が返す構造体のサイズと異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="3e1ed-135">**adrlist**構造体のメモリを割り当てるときは、各[spropvalue](spropvalue.md)構造体のメモリを個別に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="3e1ed-136">[abproviderinit](abproviderinit.md)関数に渡される MAPI メモリ割り当て関数へのポインターを使用して、メモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="3e1ed-137">adrlist の[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と\*\*\*\* 、adrlist の**adrlist**構造の各プロパティの値構造\*\*\*\* に、メモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="3e1ed-138">**address**がより大きな**adrlist**構造を返す必要がある場合、または_lppadrlist_に NULL が渡された場合、 **address**は元の構造を解放し、新しい構造を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="3e1ed-139">また、**アドレス**は**adrlist**構造に追加のプロパティ値構造を割り当て、必要に応じて古いものを解放します。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="3e1ed-140">**adrlist**構造体のメモリの管理方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="3e1ed-141">_lpadrparms_パラメーターの**ADRPARM**構造で DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに戻ります。</span><span class="sxs-lookup"><span data-stu-id="3e1ed-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e1ed-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e1ed-142">See also</span></span>



[<span data-ttu-id="3e1ed-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3e1ed-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="3e1ed-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="3e1ed-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="3e1ed-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3e1ed-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="3e1ed-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="3e1ed-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="3e1ed-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="3e1ed-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="3e1ed-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="3e1ed-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="3e1ed-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="3e1ed-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="3e1ed-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3e1ed-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3e1ed-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="3e1ed-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="3e1ed-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3e1ed-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3e1ed-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3e1ed-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3e1ed-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3e1ed-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3e1ed-155">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1ed-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="3e1ed-156">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1ed-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="3e1ed-157">PidTagDisplayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1ed-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="3e1ed-158">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1ed-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="3e1ed-159">PidTagRecipientType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1ed-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="3e1ed-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3e1ed-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3e1ed-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3e1ed-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="3e1ed-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e1ed-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="3e1ed-163">adrlist および srowset 構造のためのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="3e1ed-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

