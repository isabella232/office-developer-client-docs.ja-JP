---
title: PidTagSubmitFlags 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339355"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="5e430-103">PidTagSubmitFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e430-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5e430-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e430-105">メッセージの送信に関する詳細を示すフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e430-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e430-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5e430-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e430-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5e430-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5e430-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5e430-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e430-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="5e430-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="5e430-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5e430-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e430-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e430-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e430-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5e430-112">Area:</span></span>  <br/> |<span data-ttu-id="5e430-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="5e430-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e430-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5e430-114">Remarks</span></span>

<span data-ttu-id="5e430-115">次のフラグの 1 つ以上を、ビットマスクに **PR_SUBMIT_FLAGS** できます。</span><span class="sxs-lookup"><span data-stu-id="5e430-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="5e430-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="5e430-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="5e430-117">MAPI スプーラーは現在、メッセージがロックされています。</span><span class="sxs-lookup"><span data-stu-id="5e430-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="5e430-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="5e430-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="5e430-119">メッセージには前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="5e430-119">The message needs preprocessing.</span></span> <span data-ttu-id="5e430-120">MAPI スプーラーは、このメッセージの前処理が完了したら [、IMessage::SubmitMessage メソッドを呼び出す必要](imessage-submitmessage.md) があります。</span><span class="sxs-lookup"><span data-stu-id="5e430-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="5e430-121">メッセージ ストア プロバイダーは、スプーラーがクライアント アプリケーションではなく **SubmitMessage** を呼び出し、フラグをクリアし、メッセージの送信を続行することを認識します。</span><span class="sxs-lookup"><span data-stu-id="5e430-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5e430-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5e430-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e430-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5e430-123">Protocol specifications</span></span>

<span data-ttu-id="5e430-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e430-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e430-125">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5e430-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e430-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e430-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e430-127">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="5e430-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e430-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5e430-128">Header files</span></span>

<span data-ttu-id="5e430-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e430-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e430-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e430-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e430-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e430-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5e430-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e430-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e430-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e430-133">See also</span></span>



[<span data-ttu-id="5e430-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="5e430-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="5e430-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5e430-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e430-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e430-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e430-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e430-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e430-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5e430-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

