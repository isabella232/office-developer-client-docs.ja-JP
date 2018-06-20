---
title: PidTagStatusString の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803577"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="2db0b-103">PidTagStatusString の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2db0b-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="2db0b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2db0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2db0b-105">セッション リソースの現在の状態を示すメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2db0b-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2db0b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="2db0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2db0b-107">PR_STATUS_STRING、PR_STATUS_STRING_A、PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="2db0b-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="2db0b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2db0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2db0b-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="2db0b-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="2db0b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="2db0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2db0b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2db0b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2db0b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2db0b-112">Area:</span></span>  <br/> |<span data-ttu-id="2db0b-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="2db0b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2db0b-114">備考</span><span class="sxs-lookup"><span data-stu-id="2db0b-114">Remarks</span></span>

<span data-ttu-id="2db0b-115">これらのプロパティは、サービス ・ プロバイダー、MAPI など、統合されたアドレス帳または特定のサービス プロバイダーのセッション リソースの状態に関する特定の情報を入力する機会を提供します。</span><span class="sxs-lookup"><span data-stu-id="2db0b-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="2db0b-116">このプロパティについて説明し、ステータス コード、または**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="2db0b-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="2db0b-117">ステータスのすべてのオブジェクトに必要なは、 **PR_STATUS_CODE** 、 **PR_STATUS_STRING**および関連付けられたプロパティは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="2db0b-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="2db0b-118">トランスポート プロバイダーは、値を指定しなければ、MAPI スプーラーは、既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="2db0b-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="2db0b-119">MAPI スプーラーを無効にすると、リモート プロシージャ コールの同じ側に文字列が生成されます。プロセス境界を越えてマーシャ リングされるのではなく、共有メモリ経由とするとします。</span><span class="sxs-lookup"><span data-stu-id="2db0b-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2db0b-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2db0b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2db0b-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2db0b-121">Header files</span></span>

<span data-ttu-id="2db0b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2db0b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2db0b-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2db0b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2db0b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2db0b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2db0b-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2db0b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2db0b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2db0b-126">See also</span></span>



[<span data-ttu-id="2db0b-127">PidTagStatusCode の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="2db0b-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="2db0b-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2db0b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2db0b-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2db0b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2db0b-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="2db0b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2db0b-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2db0b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

