---
title: PidTagStatusString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421565"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="198b8-103">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="198b8-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="198b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="198b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="198b8-105">セッション リソースの現在の状態を示すメッセージが含まれる。</span><span class="sxs-lookup"><span data-stu-id="198b8-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="198b8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="198b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="198b8-107">PR_STATUS_STRING、PR_STATUS_STRING_A、PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="198b8-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="198b8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="198b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="198b8-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="198b8-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="198b8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="198b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="198b8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="198b8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="198b8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="198b8-112">Area:</span></span>  <br/> |<span data-ttu-id="198b8-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="198b8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="198b8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="198b8-114">Remarks</span></span>

<span data-ttu-id="198b8-115">これらのプロパティを使用すると、サービス プロバイダーと MAPI は、統合アドレス帳や特定のサービス プロバイダーなど、セッション リソースの状態に関する特定の情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="198b8-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="198b8-116">このプロパティは、状態コードまたはプロパティ[(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)プロパティPR_STATUS_CODE説明し、その他の情報を提供します。 </span><span class="sxs-lookup"><span data-stu-id="198b8-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="198b8-117">すべての状態 **PR_STATUS_CODE** 必要な場合は、PR_STATUS_STRING **関連付** けられているプロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="198b8-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="198b8-118">トランスポート プロバイダーが値を指定しない場合、MAPI スプーラーは既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="198b8-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="198b8-119">この文字列は、MAPI スプーラーと同じ側のリモート プロシージャ呼び出しで生成されます。プロセス境界を越えてマーシャリングされるのではなく、共有メモリを通過します。</span><span class="sxs-lookup"><span data-stu-id="198b8-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="198b8-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="198b8-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="198b8-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="198b8-121">Header files</span></span>

<span data-ttu-id="198b8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="198b8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="198b8-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="198b8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="198b8-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="198b8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="198b8-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="198b8-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="198b8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="198b8-126">See also</span></span>



[<span data-ttu-id="198b8-127">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="198b8-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="198b8-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="198b8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="198b8-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="198b8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="198b8-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="198b8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="198b8-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="198b8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

