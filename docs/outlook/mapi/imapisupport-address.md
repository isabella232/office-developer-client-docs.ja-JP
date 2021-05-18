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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407320"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="c7db7-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="c7db7-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="c7db7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7db7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7db7-105">[共通アドレス] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="c7db7-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="c7db7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c7db7-106">Parameters</span></span>

 <span data-ttu-id="c7db7-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c7db7-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="c7db7-108">[in, out]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c7db7-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="c7db7-109">入力時には、ウィンドウ ハンドルを常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7db7-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="c7db7-110">出力時に _、lpAdrParms_ パラメーターが指す [ADRPARM](adrparm.md)構造で DIALOG_SDI フラグが設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="c7db7-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="c7db7-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="c7db7-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="c7db7-112">[in, out]アドレス ダイアログ ボックスの表示と動作を制御する **ADRPARM** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c7db7-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="c7db7-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="c7db7-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="c7db7-114">[in, out]アドレス一覧へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="c7db7-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="c7db7-115">入力時に、このリストはメッセージ内の受信者の現在のリストか、そのようなリストが存在しない場合は NULL のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c7db7-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="c7db7-116">出力時に  _、lppAdrList は_ メッセージ受信者の更新されたリストをポイントします。</span><span class="sxs-lookup"><span data-stu-id="c7db7-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7db7-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="c7db7-117">Return value</span></span>

<span data-ttu-id="c7db7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7db7-118">S_OK</span></span> 
  
> <span data-ttu-id="c7db7-119">[アドレス] ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="c7db7-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7db7-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c7db7-120">Remarks</span></span>

<span data-ttu-id="c7db7-121">**IMAPISupport::Address** メソッドは、アドレス帳プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="c7db7-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="c7db7-122">アドレス帳プロバイダーは、 **アドレスを呼び出** して、メッセージ受信者のリストを作成または更新します。</span><span class="sxs-lookup"><span data-stu-id="c7db7-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="c7db7-123">各受信者は [、lppAdrList](adrentry.md) パラメーターが指す [ADRLIST](adrlist.md) 構造に含まれる  _ADRENTRY 構造で説明_ されています。</span><span class="sxs-lookup"><span data-stu-id="c7db7-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="c7db7-124">**ADRENTRY** 構造体には、受信者プロパティ値の配列が含まれます。そのうちの **1** つは受信者の種類、または PR_RECIPIENT_TYPE ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="c7db7-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="c7db7-125">この **ADRLIST** 構造体をクライアントに渡して [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)の呼び出しで _lpMods_ パラメーターとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="c7db7-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="c7db7-126">**ADRLIST** 構造体の各受信者は、プロパティ値の **1** つが PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティであることを示す解決済みか、**または未解決で、PR_ENTRYID** プロパティが見つからないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c7db7-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="c7db7-127">解決済み受信者 **には、PR_ENTRYID** に加えて、次のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c7db7-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="c7db7-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="c7db7-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="c7db7-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7db7-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="c7db7-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7db7-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c7db7-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7db7-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="c7db7-132">未解決の受信者には、通常、PR_DISPLAY_NAME **と** PR_RECIPIENT_TYPE のみを **含PR_RECIPIENT_TYPE。**</span><span class="sxs-lookup"><span data-stu-id="c7db7-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7db7-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c7db7-133">Notes to callers</span></span>

<span data-ttu-id="c7db7-134">呼 **び出し元が渡す ADRLIST** 構造は、MAPI が返す構造とは異なるサイズである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c7db7-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="c7db7-135">**ADRLIST** 構造体のメモリを割り当てる場合は [、SPropValue](spropvalue.md)構造体ごとに個別にメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7db7-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="c7db7-136">メモリを割り当てるには [、ABProviderInit](abproviderinit.md) 関数に渡される MAPI メモリ割り当て関数へのポインターを使用します。</span><span class="sxs-lookup"><span data-stu-id="c7db7-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="c7db7-137">ADRLIST の [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数を使用してメモリを割り当て **、ADRLIST** の **ADRENTRY** 構造体の各プロパティ値構造 **を割り当てる**。</span><span class="sxs-lookup"><span data-stu-id="c7db7-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="c7db7-138">Address **が大** きい **ADRLIST** 構造体を返す必要がある場合、または  _lppAdrList_ に NULL を渡した場合 **、Address** は元の構造を解放し、新しい構造体を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7db7-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="c7db7-139">**また、アドレス** は **ADRLIST** 構造に追加のプロパティ値構造を割り当て、必要に応じて古いプロパティ値構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="c7db7-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="c7db7-140">**ADRLIST** 構造体のメモリを管理する方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7db7-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="c7db7-141">**アドレス** は _、lpAdrParms_ パラメーター DIALOG_SDI **ADRPARM** 構造体にフラグが設定されている場合、すぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="c7db7-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7db7-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7db7-142">See also</span></span>



[<span data-ttu-id="c7db7-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="c7db7-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="c7db7-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c7db7-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="c7db7-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c7db7-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c7db7-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="c7db7-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="c7db7-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="c7db7-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="c7db7-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="c7db7-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="c7db7-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="c7db7-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="c7db7-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c7db7-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c7db7-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c7db7-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="c7db7-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c7db7-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c7db7-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c7db7-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="c7db7-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c7db7-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c7db7-155">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7db7-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="c7db7-156">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7db7-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="c7db7-157">PidTagDisplayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7db7-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="c7db7-158">PidTagEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7db7-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="c7db7-159">PidTagRecipientType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7db7-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="c7db7-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c7db7-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c7db7-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="c7db7-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="c7db7-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7db7-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="c7db7-163">ADRLIST および SRowSet 構造体のメモリの管理</span><span class="sxs-lookup"><span data-stu-id="c7db7-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

