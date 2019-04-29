---
title: iaddrbookaddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407908"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="e0dbe-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="e0dbe-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="e0dbe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0dbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0dbe-105">[Outlook アドレス帳] ダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="e0dbe-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0dbe-106">Parameters</span></span>

 <span data-ttu-id="e0dbe-107">_l出 uiparam_</span><span class="sxs-lookup"><span data-stu-id="e0dbe-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="e0dbe-108">[入力]ダイアログボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="e0dbe-109">入力時には、ウィンドウハンドルを常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="e0dbe-110">出力では、 _lpadrparms_パラメーターの**ulflags**メンバーが DIALOG_SDI に設定されている場合、モードレスダイアログボックスのウィンドウハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="e0dbe-111">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-111">See Remarks.</span></span> 
    
 <span data-ttu-id="e0dbe-112">_lpadrparms_</span><span class="sxs-lookup"><span data-stu-id="e0dbe-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="e0dbe-113">[入力][アドレス] ダイアログボックスの表示と動作を制御する[ADRPARM](adrparm.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="e0dbe-114">_lppadrlist_</span><span class="sxs-lookup"><span data-stu-id="e0dbe-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="e0dbe-115">[入力]受信者の情報を含む[adrlist](adrlist.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="e0dbe-116">入力時には、このパラメーターを NULL にしたり、有効なポインターをポイントしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="e0dbe-117">出力では、このパラメーターは有効な受信者情報へのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0dbe-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="e0dbe-118">Return value</span></span>

<span data-ttu-id="e0dbe-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0dbe-119">S_OK</span></span> 
  
> <span data-ttu-id="e0dbe-120">[共通アドレス] ダイアログボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0dbe-121">注釈</span><span class="sxs-lookup"><span data-stu-id="e0dbe-121">Remarks</span></span>

<span data-ttu-id="e0dbe-122">_lpadrparms_パラメーターの**ulflags**メンバーが DIALOG_SDI に設定されている場合、出力時にモードレスダイアログボックスのウィンドウハンドルの戻り値を予測します。これは Outlook では無視されます。ダイアログのモーダルバージョンは常に、Outlook 以外のクライアントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="e0dbe-123">_lppadrlist_パラメーターを使用して、MAPI によって発信者に渡された**adrlist**構造体には、各受信者に対応する1つの[adrlist](adrentry.md)構造の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="e0dbe-124">_lpMods_パラメーターの送信メッセージの[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドに渡されると、 **adrlist**構造を使用して、その受信者リストを更新できます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="e0dbe-125">**adrentry**構造体内の各**adrentry**構造には、0個以上の[spropvalue](spropvalue.md)構造体、および受信者のすべてのプロパティセットに対する1つの構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="e0dbe-126">**Address**メソッドによって提供されるダイアログボックスを使用して受信者を削除する場合は、ゼロの**spropvalue**構造が可能です。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="e0dbe-127">1つ以上の**spropvalue**構造体がある場合は、対応する**adrentry**構造を使用して、受信者を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="e0dbe-128">受信者を解決できます。これは、 **spropvalue**構造の1つが、受信者の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティ、または未解決であることを示しています。これは、 **PR_ENTRYID**プロパティがれ.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="e0dbe-129">**PR_ENTRYID**に加えて、解決された受信者には次のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="e0dbe-130">**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0dbe-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0dbe-131">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0dbe-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0dbe-132">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0dbe-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="e0dbe-133">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e0dbe-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="e0dbe-134">発信者が渡す**adrlist**構造は、MAPI が返す構造体のサイズと異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="e0dbe-135">MAPI がより大きな**adrlist**構造を返す必要がある場合は、元の構造を解放して新しい構造を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="e0dbe-136">**adrlist**構造体のメモリを割り当てるときは、各**spropvalue**構造体のメモリを個別に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="e0dbe-137">**adrlist**構造体の割り当ておよび解放方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="e0dbe-138">DIALOG_SDI フラグが_lpadrparms_パラメーターの**ADRPARM**構造の**ulflags**メンバーで設定されている場合は、すぐに**アドレス**が返されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="e0dbe-139">Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="e0dbe-140">DIALOG_SDI が無視される場合は、ダイアログのモーダルバージョンが表示され、ハンドルへのポインターは_lアウト uiparam_では想定されません。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="e0dbe-141">**Address**は**ADRPARM**構造で unicode 文字列をサポートしています。 _lpadrparms_パラメーターの**ADRPARM**の**ulflags**メンバーで AB_UNICODEUI が指定されており、それが unicode**文字列をサポートしている場合adrlist**。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="e0dbe-142">Unicode 文字列は、Outlook の [アドレス帳] ダイアログボックスに表示される前に、マルチバイト文字文字列 (MBCS) 形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0dbe-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e0dbe-143">MFCMAPI reference</span></span>

<span data-ttu-id="e0dbe-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0dbe-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e0dbe-145">**File**</span></span>|<span data-ttu-id="e0dbe-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="e0dbe-146">**Function**</span></span>|<span data-ttu-id="e0dbe-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e0dbe-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0dbe-148">MAPIStoreFunctions</span><span class="sxs-lookup"><span data-stu-id="e0dbe-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e0dbe-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="e0dbe-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="e0dbe-150">mfcmapi は、 **Address**メソッドを使用して、開くメールボックスをユーザーが選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e0dbe-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0dbe-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0dbe-151">See also</span></span>



[<span data-ttu-id="e0dbe-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="e0dbe-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="e0dbe-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e0dbe-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e0dbe-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="e0dbe-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="e0dbe-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="e0dbe-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="e0dbe-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="e0dbe-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="e0dbe-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e0dbe-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e0dbe-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e0dbe-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="e0dbe-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e0dbe-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e0dbe-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e0dbe-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e0dbe-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e0dbe-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e0dbe-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e0dbe-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e0dbe-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e0dbe-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e0dbe-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e0dbe-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="e0dbe-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e0dbe-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
<span data-ttu-id="e0dbe-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e0dbe-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

