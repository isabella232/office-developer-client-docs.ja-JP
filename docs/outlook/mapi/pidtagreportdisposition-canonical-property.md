---
title: PidTagReportDisposition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346355"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="435e6-103">PidTagReportDisposition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="435e6-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="435e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="435e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="435e6-105">受信確認を要求するメッセージの受信状態を示します。</span><span class="sxs-lookup"><span data-stu-id="435e6-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="435e6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="435e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="435e6-107">PR_REPORT_DISPOSITION、PR_REPORT_DISPOSITION_A、PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="435e6-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="435e6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="435e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="435e6-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="435e6-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="435e6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="435e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="435e6-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="435e6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="435e6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="435e6-112">Area:</span></span>  <br/> |<span data-ttu-id="435e6-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="435e6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="435e6-114">解説</span><span class="sxs-lookup"><span data-stu-id="435e6-114">Remarks</span></span>

<span data-ttu-id="435e6-115">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="435e6-115">The following are valid values:</span></span>
  
- <span data-ttu-id="435e6-116">れる</span><span class="sxs-lookup"><span data-stu-id="435e6-116">"deleted"</span></span>
    
- <span data-ttu-id="435e6-117">実行</span><span class="sxs-lookup"><span data-stu-id="435e6-117">"processed"</span></span>
    
- <span data-ttu-id="435e6-118">ディスパッチ</span><span class="sxs-lookup"><span data-stu-id="435e6-118">"dispatched"</span></span>
    
- <span data-ttu-id="435e6-119">権限</span><span class="sxs-lookup"><span data-stu-id="435e6-119">"denied"</span></span>
    
- <span data-ttu-id="435e6-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="435e6-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="435e6-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="435e6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="435e6-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="435e6-122">Protocol specifications</span></span>

<span data-ttu-id="435e6-123">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="435e6-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="435e6-124">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="435e6-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="435e6-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="435e6-125">Header files</span></span>

<span data-ttu-id="435e6-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="435e6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="435e6-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="435e6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="435e6-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="435e6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="435e6-129">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="435e6-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="435e6-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="435e6-130">See also</span></span>



[<span data-ttu-id="435e6-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="435e6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="435e6-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="435e6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="435e6-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="435e6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="435e6-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="435e6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

