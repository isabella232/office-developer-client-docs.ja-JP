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
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803801"
---
# <a name="rtfsync"></a><span data-ttu-id="64658-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="64658-103">RTFSync</span></span>

<span data-ttu-id="64658-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64658-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64658-105">リッチ テキスト形式 (RTF) メッセージのテキストがテキスト形式のバージョンと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="64658-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="64658-106">RTF 形式を読み取る前に、RTF 形式を変更した後にこの関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="64658-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64658-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="64658-107">Header file:</span></span>  <br/> |<span data-ttu-id="64658-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="64658-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="64658-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="64658-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="64658-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="64658-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="64658-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="64658-111">Called by:</span></span>  <br/> |<span data-ttu-id="64658-112">Rtf 形式に対応したクライアント アプリケーション、およびメッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="64658-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="64658-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="64658-113">Parameters</span></span>

<span data-ttu-id="64658-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="64658-114">_lpMessage_</span></span>
  
> <span data-ttu-id="64658-115">[in]更新するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="64658-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="64658-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64658-116">_ulFlags_</span></span>
  
> <span data-ttu-id="64658-117">[in]Rtf 形式またはテキスト形式のメッセージを示すために使用するフラグのビットが変更されています。</span><span class="sxs-lookup"><span data-stu-id="64658-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="64658-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="64658-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="64658-119">RTF_SYNC_BODY_CHANGED: メッセージのテキスト形式のバージョンが変更されました。</span><span class="sxs-lookup"><span data-stu-id="64658-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="64658-120">RTF_SYNC_RTF_CHANGED: RTF 形式のメッセージが変更されました。</span><span class="sxs-lookup"><span data-stu-id="64658-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="64658-121">_UlFlags_パラメーターで他のすべてのビットは、将来使用するために予約されています。</span><span class="sxs-lookup"><span data-stu-id="64658-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="64658-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="64658-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="64658-123">[out]更新されたメッセージが表示されるかどうかを示す変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="64658-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="64658-124">TRUE を指定するとメッセージが表示される更新された、FALSE それ以外の場合。</span><span class="sxs-lookup"><span data-stu-id="64658-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="64658-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="64658-125">Return value</span></span>

<span data-ttu-id="64658-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="64658-126">S_OK</span></span> 
  
> <span data-ttu-id="64658-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="64658-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64658-128">����</span><span class="sxs-lookup"><span data-stu-id="64658-128">Remarks</span></span>

<span data-ttu-id="64658-129">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティが存在しないか、FALSE が使用され、RTF_SYNC_BODY_ のプロパティを読み取って、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))**へ**の関数を呼び出す必要があります前にフラグが設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="64658-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="64658-130">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティでは、STORE_RTF_OK フラグは設定されていない場合、RTF_SYNC_RTF_CHANGED フラグが設定されている**PR_RTF_COMPRESSED**を変更した後でこの関数が呼び出さ 必要があります。</span><span class="sxs-lookup"><span data-stu-id="64658-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="64658-131">([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**と**PR_RTF_COMPRESSED**の両方が変更されている場合両方のフラグが設定を**行う**関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="64658-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="64658-132">_LpfMessageUpdated_パラメーターの値は、TRUE に設定されている場合、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="64658-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="64658-133">**SaveChanges**が呼び出されない場合、メッセージの変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="64658-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="64658-134">メッセージ ストア プロバイダーは、 **PR_BODY**と**PR_RTF_COMPRESSED**プロパティの同期を維持するのに、**行う**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="64658-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="64658-135">詳細については、[メッセージ ストア プロバイダーの rtf 形式のテキストをサポートしている](supporting-rtf-text-for-message-store-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64658-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64658-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="64658-136">See also</span></span>

- [<span data-ttu-id="64658-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="64658-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

