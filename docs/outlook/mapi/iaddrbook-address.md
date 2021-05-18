---
title: IAddrBookAddress
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
# <a name="iaddrbookaddress"></a><span data-ttu-id="4467f-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="4467f-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="4467f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4467f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4467f-105">[Outlook アドレス帳] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4467f-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="4467f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4467f-106">Parameters</span></span>

 <span data-ttu-id="4467f-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4467f-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="4467f-108">[in, out]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4467f-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="4467f-109">入力時には、ウィンドウ ハンドルを常に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="4467f-110">出力時に _、lpAdrParms_ パラメーターの **ulFlags** メンバーが DIALOG_SDI に設定されている場合、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="4467f-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="4467f-111">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4467f-111">See Remarks.</span></span> 
    
 <span data-ttu-id="4467f-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="4467f-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="4467f-113">[in, out]アドレス ダイアログ ボックスの表示と動作を制御する [ADRPARM](adrparm.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4467f-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="4467f-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="4467f-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="4467f-115">[in, out]受信者情報を含む [ADRLIST](adrlist.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4467f-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="4467f-116">入力時に、このパラメーターは NULL または有効なポインターをポイントできます。</span><span class="sxs-lookup"><span data-stu-id="4467f-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="4467f-117">出力時に、このパラメーターは有効な受信者情報へのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="4467f-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4467f-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="4467f-118">Return value</span></span>

<span data-ttu-id="4467f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4467f-119">S_OK</span></span> 
  
> <span data-ttu-id="4467f-120">[共通アドレス] ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="4467f-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4467f-121">注釈</span><span class="sxs-lookup"><span data-stu-id="4467f-121">Remarks</span></span>

<span data-ttu-id="4467f-122">_lpAdrParms_ パラメーターの **ulFlags** メンバーが出力時のモードレス ダイアログ ボックスのウィンドウ ハンドルの戻り値を予期して DIALOG_SDI に設定されている場合、Outlook では無視されます。ダイアログのモーダル バージョンは常に Outlook 以外のクライアントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4467f-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="4467f-123">_LppAdrList_ パラメーターを介して呼び出し元に MAPI によって渡される **ADRLIST** 構造体には [、ADRENTRY](adrentry.md)構造体の配列が含まれています。受信者ごとに 1 つの構造です。</span><span class="sxs-lookup"><span data-stu-id="4467f-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="4467f-124">_lpMods_ パラメーターで送信メッセージの [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドに渡された場合 **、ADRLIST** 構造を使用して受信者リストを更新できます。</span><span class="sxs-lookup"><span data-stu-id="4467f-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="4467f-125">ADRLIST 構造体 **内の** 各 **ADRENTRY** 構造には、受信者に設定されたプロパティごとに 1 つの構造である 0 個以上の [SPropValue](spropvalue.md) 構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4467f-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="4467f-126">Address メソッドによって表示されるダイアログ ボックスを使用して受信者を削除すると **、SPropValue** 構造体が 0 になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="4467f-127">1 つ以上の **SPropValue** 構造体がある場合、対応する **ADRENTRY** 構造体を使用して受信者を追加または更新します。</span><span class="sxs-lookup"><span data-stu-id="4467f-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="4467f-128">受信者は解決できます。 **これは、SPropValue** 構造体の 1 つが受信者の **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティ、または未解決を表し **、PR_ENTRYID** プロパティが見つからないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="4467f-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="4467f-129">解決済み受信者 **には、PR_ENTRYID** に加えて、次のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4467f-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="4467f-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4467f-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="4467f-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4467f-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="4467f-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4467f-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="4467f-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4467f-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="4467f-134">呼 **び出し元が渡す ADRLIST** 構造は、MAPI が返す構造とは異なるサイズである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="4467f-135">MAPI は、より大きな **ADRLIST** 構造を返す必要がある場合、元の構造を解放し、新しい構造を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="4467f-136">**ADRLIST** 構造体のメモリを割り当てる場合は **、SPropValue** 構造体ごとに個別にメモリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="4467f-137">ADRLIST 構造体を割り当て、解放する方法の詳細については **、「ADRLIST** および SRowSet 構造体のメモリの管理」 [を参照してください。](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="4467f-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="4467f-138"> _lpAdrParms_ パラメーター DIALOG_SDI **ADRPARM** 構造体の **ulFlags** メンバーにフラグが設定されている場合、アドレスは直ちに返します。</span><span class="sxs-lookup"><span data-stu-id="4467f-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="4467f-139">Outlook DIALOG_SDIの場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4467f-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="4467f-140">このDIALOG_SDIを無視すると、モーダル バージョンのダイアログが表示され  _、lpulUIParam_ でハンドルへのポインターを予期しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="4467f-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="4467f-141">アドレスは _、lpAdrParms_ パラメーターの ADRPARM の **ulFlags** メンバーで AB_UNICODEUI が指定されている場合 **、ADRPARM** 構造体の Unicode 文字文字列をサポートし **、ADRLIST** で Unicode 文字文字列をサポートします。 </span><span class="sxs-lookup"><span data-stu-id="4467f-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="4467f-142">Unicode 文字列は、Outlook アドレス帳ダイアログ ボックスに表示される前に、マルチバイト文字列 (MBCS) 形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="4467f-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4467f-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4467f-143">MFCMAPI reference</span></span>

<span data-ttu-id="4467f-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4467f-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4467f-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4467f-145">**File**</span></span>|<span data-ttu-id="4467f-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="4467f-146">**Function**</span></span>|<span data-ttu-id="4467f-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4467f-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4467f-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4467f-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4467f-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="4467f-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="4467f-150">MFCMAPI は **Address メソッドを使用** して、ユーザーが開くメールボックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="4467f-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4467f-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="4467f-151">See also</span></span>



[<span data-ttu-id="4467f-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="4467f-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="4467f-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="4467f-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="4467f-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="4467f-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="4467f-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="4467f-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="4467f-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="4467f-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="4467f-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="4467f-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="4467f-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="4467f-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="4467f-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4467f-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4467f-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="4467f-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="4467f-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4467f-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4467f-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4467f-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="4467f-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4467f-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="4467f-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4467f-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="4467f-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4467f-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
<span data-ttu-id="4467f-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4467f-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

