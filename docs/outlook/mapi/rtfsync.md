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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316481"
---
# <a name="rtfsync"></a><span data-ttu-id="197db-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="197db-103">RTFSync</span></span>

<span data-ttu-id="197db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="197db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="197db-105">リッチテキスト形式 (RTF) のメッセージテキストがプレーンテキストバージョンと一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="197db-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="197db-106">rtf バージョンを読み取る前に、または rtf バージョンを変更した後に、この関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="197db-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="197db-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="197db-107">Header file:</span></span>  <br/> |<span data-ttu-id="197db-108">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="197db-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="197db-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="197db-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="197db-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="197db-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="197db-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="197db-111">Called by:</span></span>  <br/> |<span data-ttu-id="197db-112">RTF 対応クライアントアプリケーションとメッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="197db-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="197db-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="197db-113">Parameters</span></span>

<span data-ttu-id="197db-114">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="197db-114">_lpMessage_</span></span>
  
> <span data-ttu-id="197db-115">順番更新するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="197db-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="197db-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="197db-116">_ulFlags_</span></span>
  
> <span data-ttu-id="197db-117">順番メッセージの RTF またはプレーンテキストのバージョンが変更されたことを示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="197db-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="197db-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="197db-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="197db-119">RTF_SYNC_BODY_CHANGED: メッセージのテキスト形式のバージョンが変更されました。</span><span class="sxs-lookup"><span data-stu-id="197db-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="197db-120">RTF_SYNC_RTF_CHANGED: メッセージの RTF バージョンが変更されました。</span><span class="sxs-lookup"><span data-stu-id="197db-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="197db-121">_ulflags_パラメーターの他のすべてのビットは、今後の使用のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="197db-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="197db-122">_lpfmessageupdated_</span><span class="sxs-lookup"><span data-stu-id="197db-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="197db-123">読み上げ更新されたメッセージがあるかどうかを示す変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="197db-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="197db-124">更新されたメッセージがある場合は TRUE、それ以外の場合は FALSE。</span><span class="sxs-lookup"><span data-stu-id="197db-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="197db-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="197db-125">Return value</span></span>

<span data-ttu-id="197db-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="197db-126">S_OK</span></span> 
  
> <span data-ttu-id="197db-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="197db-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="197db-128">解説</span><span class="sxs-lookup"><span data-stu-id="197db-128">Remarks</span></span>

<span data-ttu-id="197db-129">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが存在しないか FALSE の場合は、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを読み取る前に、RTF_SYNC_BODY_ を使用して**rtfsync**関数を呼び出す必要があります。フラグセットが変更されました。</span><span class="sxs-lookup"><span data-stu-id="197db-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="197db-130">STORE_RTF_OK フラグが**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで設定されていない場合、この関数は、 **PR_RTF_COMPRESSED**の変更後に RTF_SYNC_RTF_CHANGED フラグセットを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="197db-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="197db-131">**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) と**PR_RTF_COMPRESSED**の両方が変更されている場合は、両方の flags セットを使用して**rtfsync**関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="197db-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="197db-132">_lpfmessageupdated_パラメーターの値が TRUE に設定されている場合は、メッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="197db-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="197db-133">**SaveChanges**が呼び出されていない場合、変更はメッセージに保存されません。</span><span class="sxs-lookup"><span data-stu-id="197db-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="197db-134">メッセージストアプロバイダーは、 **rtfsync**を使用して、 **PR_BODY**プロパティと**PR_RTF_COMPRESSED**プロパティを同期させておくことができます。</span><span class="sxs-lookup"><span data-stu-id="197db-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="197db-135">詳細については、「[メッセージストアプロバイダー用の RTF テキストのサポート](supporting-rtf-text-for-message-store-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="197db-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="197db-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="197db-136">See also</span></span>

- [<span data-ttu-id="197db-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="197db-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

