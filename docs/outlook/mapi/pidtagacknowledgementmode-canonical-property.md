---
title: PidTagAcknowledgementMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAcknowledgementMode
api_type:
- HeaderDef
ms.assetid: 23329ca3-89f9-4e5a-9c8a-6262f2a2d26f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cee99b93d41ac8cd4a3dee18cad6cd4ab01cabe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335282"
---
# <a name="pidtagacknowledgementmode-canonical-property"></a><span data-ttu-id="1e642-103">PidTagAcknowledgementMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e642-103">PidTagAcknowledgementMode Canonical Property</span></span>

  
  
<span data-ttu-id="1e642-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e642-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e642-105">メッセージ受信のモードの識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="1e642-105">Contains the identifier of the mode for message acknowledgment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e642-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1e642-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e642-107">PR_ACKNOWLEDGEMENT_MODE</span><span class="sxs-lookup"><span data-stu-id="1e642-107">PR_ACKNOWLEDGEMENT_MODE</span></span>  <br/> |
|<span data-ttu-id="1e642-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1e642-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e642-109">0x0001</span><span class="sxs-lookup"><span data-stu-id="1e642-109">0x0001</span></span>  <br/> |
|<span data-ttu-id="1e642-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1e642-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e642-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e642-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e642-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1e642-112">Area:</span></span>  <br/> |<span data-ttu-id="1e642-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="1e642-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e642-114">解説</span><span class="sxs-lookup"><span data-stu-id="1e642-114">Remarks</span></span>

<span data-ttu-id="1e642-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1e642-115">This property can have exactly one of the following values:</span></span>
  
|<span data-ttu-id="1e642-116">**値**</span><span class="sxs-lookup"><span data-stu-id="1e642-116">**Value**</span></span>|<span data-ttu-id="1e642-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e642-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1e642-118">.0</span><span class="sxs-lookup"><span data-stu-id="1e642-118">0</span></span>  <br/> |<span data-ttu-id="1e642-119">手動での受信確認。</span><span class="sxs-lookup"><span data-stu-id="1e642-119">Manual acknowledgment.</span></span>  <br/> |
|<span data-ttu-id="1e642-120">1-d</span><span class="sxs-lookup"><span data-stu-id="1e642-120">1</span></span>  <br/> |<span data-ttu-id="1e642-121">自動応答。</span><span class="sxs-lookup"><span data-stu-id="1e642-121">Automatic acknowledgment.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1e642-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1e642-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1e642-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1e642-123">Header files</span></span>

<span data-ttu-id="1e642-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e642-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e642-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e642-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e642-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1e642-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1e642-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e642-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e642-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e642-128">See also</span></span>



[<span data-ttu-id="1e642-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1e642-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e642-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e642-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e642-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e642-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e642-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e642-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

