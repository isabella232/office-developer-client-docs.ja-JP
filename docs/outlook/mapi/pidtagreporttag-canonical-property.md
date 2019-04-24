---
title: PidTagReportTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331431"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="159f9-103">PidTagReportTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="159f9-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="159f9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="159f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="159f9-105">メッセージに対して生成されたレポートにメッセージングシステムがコピーするバイナリタグの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="159f9-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="159f9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="159f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="159f9-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="159f9-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="159f9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="159f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="159f9-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="159f9-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="159f9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="159f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="159f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="159f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="159f9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="159f9-112">Area:</span></span>  <br/> |<span data-ttu-id="159f9-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="159f9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="159f9-114">解説</span><span class="sxs-lookup"><span data-stu-id="159f9-114">Remarks</span></span>

<span data-ttu-id="159f9-115">**PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) プロパティなどのこのプロパティを使用して、レポートと元のメッセージを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="159f9-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="159f9-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="159f9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="159f9-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="159f9-117">Protocol specifications</span></span>

<span data-ttu-id="159f9-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="159f9-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="159f9-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="159f9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="159f9-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="159f9-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="159f9-121">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="159f9-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="159f9-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="159f9-122">Header files</span></span>

<span data-ttu-id="159f9-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="159f9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="159f9-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="159f9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="159f9-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="159f9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="159f9-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="159f9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="159f9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="159f9-127">See also</span></span>



[<span data-ttu-id="159f9-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="159f9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="159f9-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="159f9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="159f9-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="159f9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="159f9-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="159f9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

