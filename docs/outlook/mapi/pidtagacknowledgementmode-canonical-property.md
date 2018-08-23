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
ms.openlocfilehash: 28b42e6abee5d918dbcca69c13642f3ebcc859e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581938"
---
# <a name="pidtagacknowledgementmode-canonical-property"></a><span data-ttu-id="b64e9-103">PidTagAcknowledgementMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b64e9-103">PidTagAcknowledgementMode Canonical Property</span></span>

  
  
<span data-ttu-id="b64e9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b64e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b64e9-105">メッセージの受信確認モードの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b64e9-105">Contains the identifier of the mode for message acknowledgment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b64e9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b64e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b64e9-107">PR_ACKNOWLEDGEMENT_MODE</span><span class="sxs-lookup"><span data-stu-id="b64e9-107">PR_ACKNOWLEDGEMENT_MODE</span></span>  <br/> |
|<span data-ttu-id="b64e9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b64e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b64e9-109">0x0001</span><span class="sxs-lookup"><span data-stu-id="b64e9-109">0x0001</span></span>  <br/> |
|<span data-ttu-id="b64e9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b64e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b64e9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b64e9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b64e9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b64e9-112">Area:</span></span>  <br/> |<span data-ttu-id="b64e9-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="b64e9-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b64e9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b64e9-114">Remarks</span></span>

<span data-ttu-id="b64e9-115">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b64e9-115">This property can have exactly one of the following values:</span></span>
  
|<span data-ttu-id="b64e9-116">**値**</span><span class="sxs-lookup"><span data-stu-id="b64e9-116">**Value**</span></span>|<span data-ttu-id="b64e9-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="b64e9-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b64e9-118">0</span><span class="sxs-lookup"><span data-stu-id="b64e9-118">0</span></span>  <br/> |<span data-ttu-id="b64e9-119">手動受信を確認します。</span><span class="sxs-lookup"><span data-stu-id="b64e9-119">Manual acknowledgment.</span></span>  <br/> |
|<span data-ttu-id="b64e9-120">1</span><span class="sxs-lookup"><span data-stu-id="b64e9-120">1</span></span>  <br/> |<span data-ttu-id="b64e9-121">自動受信を確認します。</span><span class="sxs-lookup"><span data-stu-id="b64e9-121">Automatic acknowledgment.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b64e9-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b64e9-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b64e9-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b64e9-123">Header files</span></span>

<span data-ttu-id="b64e9-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b64e9-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b64e9-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b64e9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b64e9-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b64e9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b64e9-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b64e9-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b64e9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b64e9-128">See also</span></span>



[<span data-ttu-id="b64e9-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b64e9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b64e9-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b64e9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b64e9-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b64e9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b64e9-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b64e9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

