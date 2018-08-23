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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579957"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="292cc-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="292cc-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="292cc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="292cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="292cc-105">Outlook アドレス帳] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="292cc-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="292cc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="292cc-106">Parameters</span></span>

 <span data-ttu-id="292cc-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="292cc-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="292cc-108">[で [チェック アウト]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="292cc-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="292cc-109">入力、ウィンドウ ハンドルを渡す必要が常にあります。</span><span class="sxs-lookup"><span data-stu-id="292cc-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="292cc-110">出力、DIALOG_SDI に、 **ulFlags**のメンバー、 _lpAdrParms_パラメーターが設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。</span><span class="sxs-lookup"><span data-stu-id="292cc-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="292cc-111">注釈を参照してください。</span><span class="sxs-lookup"><span data-stu-id="292cc-111">See Remarks.</span></span> 
    
 <span data-ttu-id="292cc-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="292cc-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="292cc-113">[で [チェック アウト]プレゼンテーションと、[アドレス] ダイアログ ボックスの動作を制御する[ADRPARM](adrparm.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="292cc-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="292cc-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="292cc-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="292cc-115">[で [チェック アウト]受信者の情報を格納する[ADRLIST](adrlist.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="292cc-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="292cc-116">入力の場合、このパラメーターが NULL または有効なポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="292cc-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="292cc-117">出力では、このパラメーターは、有効な受信者情報へのポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="292cc-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="292cc-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="292cc-118">Return value</span></span>

<span data-ttu-id="292cc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="292cc-119">S_OK</span></span> 
  
> <span data-ttu-id="292cc-120">共通のアドレス] ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="292cc-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="292cc-121">注釈</span><span class="sxs-lookup"><span data-stu-id="292cc-121">Remarks</span></span>

<span data-ttu-id="292cc-122">Outlook では無視されます、 **ulFlags**のメンバー、 _lpAdrParms_パラメーターは、出力時に、モードレス ダイアログ ボックスのウィンドウ ハンドルの戻り値を予測し DIALOG_SDI に設定されている場合Outlook 以外のクライアントでは、モーダル ダイアログ ボックスのバージョンは常に表示します。</span><span class="sxs-lookup"><span data-stu-id="292cc-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="292cc-123">_LppAdrList_パラメーターを通じて呼び出し元に、MAPI によって渡される**ADRLIST**構造体には、受信者ごとに 1 つの構造、 [ADRENTRY](adrentry.md)の構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="292cc-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="292cc-124">_LpMods_パラメーターでの送信メッセージの[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドに渡されると、その受信者のリストを更新する**ADRLIST**構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="292cc-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="292cc-125">**ADRLIST**構造内の個々 の**ADRENTRY**構造体には、0 個以上の[SPropValue](spropvalue.md)構造体、すべてのプロパティの設定、受信者の 1 つの構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="292cc-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="292cc-126">受信者を削除する**アドレス**の方法で表示されるダイアログ ボックスを使用する場合、0 **SPropValue**構造体が存在することができます。</span><span class="sxs-lookup"><span data-stu-id="292cc-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="292cc-127">**SPropValue**構造体が 1 つまたは複数が存在する場合、対応する**ADRENTRY**構造体を使用して、追加または受信者を更新します。</span><span class="sxs-lookup"><span data-stu-id="292cc-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="292cc-128">受信者を解決できるを示すこと**SPropValue**構造体のいずれかの受信者の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティの説明、未解決の**PR_ENTRYID**プロパティがあることを示します不足しています。</span><span class="sxs-lookup"><span data-stu-id="292cc-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="292cc-129">**PR_ENTRYID**、他は、解決の受信者には、次のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="292cc-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="292cc-130">**PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="292cc-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="292cc-131">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="292cc-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="292cc-132">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="292cc-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="292cc-133">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="292cc-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="292cc-134">**ADRLIST**構造で、呼び出し元に合格するには、MAPI を表す構造体のサイズが異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="292cc-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="292cc-135">MAPI より大きな**ADRLIST**の構造体を返す必要がある場合に、元の構造体を解放し、新しい 1 を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="292cc-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="292cc-136">**ADRLIST**構造体のメモリを割り当てるときに、個別に各**SPropValue**構造体のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="292cc-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="292cc-137">割り当てるし、 **ADRLIST**構造体を解放する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="292cc-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="292cc-138">**UlFlags** 、 **ADRPARM**構造体のメンバーに、 _lpAdrParms_パラメーターに DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに返します。</span><span class="sxs-lookup"><span data-stu-id="292cc-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="292cc-139">Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="292cc-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="292cc-140">DIALOG_SDI は無視されますが場合、は、モーダル ダイアログ ボックスのバージョンが表示され、ハンドルへのポインターは、 _lpulUIParam_で予期しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="292cc-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="292cc-141">**アドレス**をサポートしている文字の Unicode 文字列**ADRPARM**構造体の AB_UNICODEUI は、 _lpAdrParms_パラメーターには、 **ADRPARM**の**ulFlags**メンバーで指定された**では、Unicode 文字列をサポートしている場合ADRLIST**。</span><span class="sxs-lookup"><span data-stu-id="292cc-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="292cc-142">Unicode 文字列は、Outlook アドレス帳] ダイアログ ボックスに表示される前に、マルチバイト文字 (MBCS) の文字列形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="292cc-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="292cc-143">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="292cc-143">MFCMAPI reference</span></span>

<span data-ttu-id="292cc-144">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="292cc-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="292cc-145">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="292cc-145">**File**</span></span>|<span data-ttu-id="292cc-146">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="292cc-146">**Function**</span></span>|<span data-ttu-id="292cc-147">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="292cc-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="292cc-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="292cc-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="292cc-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="292cc-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="292cc-150">MFCMAPI では、**アドレス**メソッドを使用して、ユーザーがどのメールボックスを開くを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="292cc-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="292cc-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="292cc-151">See also</span></span>



[<span data-ttu-id="292cc-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="292cc-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="292cc-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="292cc-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="292cc-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="292cc-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="292cc-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="292cc-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="292cc-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="292cc-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="292cc-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="292cc-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="292cc-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="292cc-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="292cc-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="292cc-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="292cc-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="292cc-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="292cc-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="292cc-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="292cc-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="292cc-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="292cc-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="292cc-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="292cc-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="292cc-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="292cc-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="292cc-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
<span data-ttu-id="292cc-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="292cc-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

