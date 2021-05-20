---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436210"
---
# <a name="rtfsync"></a><span data-ttu-id="9b1de-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="9b1de-103">RTFSync</span></span>

<span data-ttu-id="9b1de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b1de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b1de-105">リッチ テキスト形式 (RTF) メッセージ テキストがプレーン テキスト のバージョンと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b1de-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="9b1de-106">RTF バージョンを読み取る前と RTF バージョンを変更した後に、この関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b1de-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b1de-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9b1de-107">Header file:</span></span>  <br/> |<span data-ttu-id="9b1de-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9b1de-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9b1de-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="9b1de-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b1de-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9b1de-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9b1de-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="9b1de-111">Called by:</span></span>  <br/> |<span data-ttu-id="9b1de-112">RTF 対応のクライアント アプリケーションとメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9b1de-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="9b1de-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b1de-113">Parameters</span></span>

<span data-ttu-id="9b1de-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9b1de-114">_lpMessage_</span></span>
  
> <span data-ttu-id="9b1de-115">[in]更新するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b1de-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="9b1de-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b1de-116">_ulFlags_</span></span>
  
> <span data-ttu-id="9b1de-117">[in]メッセージの RTF またはプレーン テキスト バージョンを示すために使用されるフラグのビットマスクが変更されました。</span><span class="sxs-lookup"><span data-stu-id="9b1de-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="9b1de-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9b1de-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="9b1de-119">RTF_SYNC_BODY_CHANGED: メッセージのプレーン テキスト バージョンが変更されました。</span><span class="sxs-lookup"><span data-stu-id="9b1de-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="9b1de-120">RTF_SYNC_RTF_CHANGED: メッセージの RTF バージョンが変更されました。</span><span class="sxs-lookup"><span data-stu-id="9b1de-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="9b1de-121">_ulFlags_ パラメーター内の他のすべてのビットは、将来の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="9b1de-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="9b1de-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="9b1de-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="9b1de-123">[out]更新されたメッセージが存在するかどうかを示す変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b1de-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="9b1de-124">更新されたメッセージがある場合は TRUE、それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="9b1de-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b1de-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="9b1de-125">Return value</span></span>

<span data-ttu-id="9b1de-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b1de-126">S_OK</span></span> 
  
> <span data-ttu-id="9b1de-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9b1de-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b1de-128">注釈</span><span class="sxs-lookup"><span data-stu-id="9b1de-128">Remarks</span></span>

<span data-ttu-id="9b1de-129">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが見つからないか、FALSE の場合は、PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを読み取る前に **、RTFSync** 関数を RTF_SYNC_BODY_CHANGED フラグ セットで呼び出す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="9b1de-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="9b1de-130">PR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで **STORE_RTF_OK** フラグが設定されていない場合、この関数は、PR_RTF_COMPRESSED を変更した後に RTF_SYNC_RTF_CHANGED フラグを設定して **呼び出す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="9b1de-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="9b1de-131">両方の **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) と PR_RTF_COMPRESSED変更されている場合は、両方のフラグ **を** 設定して **RTFSync** 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b1de-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="9b1de-132">_lpfMessageUpdated_ パラメーターの値が TRUE に設定されている場合は、メッセージに対して [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b1de-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="9b1de-133">**SaveChanges が** 呼び出されない場合、変更はメッセージに保存されません。</span><span class="sxs-lookup"><span data-stu-id="9b1de-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="9b1de-134">メッセージ ストア プロバイダーは **、RTFSync** を使用して、PR_BODY **プロパティPR_RTF_COMPRESSED\*\*\*\*維持できます**。</span><span class="sxs-lookup"><span data-stu-id="9b1de-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="9b1de-135">詳細については、「メッセージ ストア プロバイダー [の RTF テキストのサポート」を参照してください](supporting-rtf-text-for-message-store-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="9b1de-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b1de-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b1de-136">See also</span></span>

- [<span data-ttu-id="9b1de-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="9b1de-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

