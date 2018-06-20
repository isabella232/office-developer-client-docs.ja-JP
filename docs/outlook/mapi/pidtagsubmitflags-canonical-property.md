---
title: PidTagSubmitFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803615"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="afe5d-103">PidTagSubmitFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="afe5d-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="afe5d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afe5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afe5d-105">メッセージの送信に関する詳細情報を示すフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="afe5d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="afe5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afe5d-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="afe5d-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="afe5d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="afe5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afe5d-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="afe5d-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="afe5d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="afe5d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="afe5d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="afe5d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="afe5d-112">Area:</span></span>  <br/> |<span data-ttu-id="afe5d-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="afe5d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afe5d-114">備考</span><span class="sxs-lookup"><span data-stu-id="afe5d-114">Remarks</span></span>

<span data-ttu-id="afe5d-115">**PR_SUBMIT_FLAGS**ビットマスクについては、次のフラグの 1 つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="afe5d-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="afe5d-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="afe5d-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="afe5d-117">MAPI スプーラーは、現在ロックされているメッセージを持ちます。</span><span class="sxs-lookup"><span data-stu-id="afe5d-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="afe5d-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="afe5d-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="afe5d-119">メッセージでは、前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="afe5d-119">The message needs preprocessing.</span></span> <span data-ttu-id="afe5d-120">MAPI スプーラーが終了するとこのメッセージを処理するには、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="afe5d-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="afe5d-121">メッセージ ストア プロバイダーは、クライアント ・ アプリケーションではなく、スプーラーでは、 **SubmitMessage**と呼ばれる、フラグをクリア、メッセージの送信を続行を認識します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="afe5d-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="afe5d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afe5d-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="afe5d-123">Protocol specifications</span></span>

<span data-ttu-id="afe5d-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afe5d-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afe5d-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="afe5d-126">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afe5d-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afe5d-127">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afe5d-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="afe5d-128">Header files</span></span>

<span data-ttu-id="afe5d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="afe5d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="afe5d-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="afe5d-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="afe5d-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="afe5d-131">Mapitags.h</span></span>
  
> <span data-ttu-id="afe5d-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="afe5d-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afe5d-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="afe5d-133">See also</span></span>



[<span data-ttu-id="afe5d-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="afe5d-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="afe5d-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="afe5d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afe5d-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="afe5d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afe5d-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="afe5d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afe5d-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="afe5d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

