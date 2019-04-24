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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339355"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="a137a-103">PidTagSubmitFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a137a-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a137a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a137a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a137a-105">メッセージ送信に関する詳細を示すフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="a137a-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a137a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a137a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a137a-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a137a-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a137a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a137a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a137a-109">0x0e14</span><span class="sxs-lookup"><span data-stu-id="a137a-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="a137a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a137a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a137a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a137a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a137a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a137a-112">Area:</span></span>  <br/> |<span data-ttu-id="a137a-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="a137a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a137a-114">解説</span><span class="sxs-lookup"><span data-stu-id="a137a-114">Remarks</span></span>

<span data-ttu-id="a137a-115">**PR_SUBMIT_FLAGS**ビットマスクには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a137a-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="a137a-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="a137a-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="a137a-117">MAPI スプーラーには、現在メッセージがロックされています。</span><span class="sxs-lookup"><span data-stu-id="a137a-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="a137a-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="a137a-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="a137a-119">メッセージに前処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="a137a-119">The message needs preprocessing.</span></span> <span data-ttu-id="a137a-120">MAPI スプーラーがこのメッセージの前処理を完了すると、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a137a-121">メッセージストアプロバイダーは、クライアントアプリケーションではなく、スプーラーが**submitmessage**を呼び出し、フラグをクリアし、メッセージ送信を続行することを認識します。</span><span class="sxs-lookup"><span data-stu-id="a137a-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a137a-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a137a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a137a-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a137a-123">Protocol specifications</span></span>

<span data-ttu-id="a137a-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a137a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a137a-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a137a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a137a-126">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a137a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a137a-127">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="a137a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a137a-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a137a-128">Header files</span></span>

<span data-ttu-id="a137a-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a137a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a137a-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a137a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a137a-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a137a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a137a-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a137a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a137a-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a137a-133">See also</span></span>



[<span data-ttu-id="a137a-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="a137a-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="a137a-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a137a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a137a-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a137a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a137a-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a137a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a137a-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a137a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

