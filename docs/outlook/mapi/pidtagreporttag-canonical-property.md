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
ms.openlocfilehash: a328d71aef57f85a5bd33db5cc219dff181dafc0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593306"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="ff03f-103">PidTagReportTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff03f-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="ff03f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff03f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff03f-105">メッセージング システムがメッセージに対して生成されたすべてのレポートをコピーする必要がありますが、バイナリのタグの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ff03f-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff03f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ff03f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff03f-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="ff03f-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="ff03f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ff03f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff03f-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="ff03f-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="ff03f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ff03f-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff03f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff03f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff03f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ff03f-112">Area:</span></span>  <br/> |<span data-ttu-id="ff03f-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="ff03f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff03f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ff03f-114">Remarks</span></span>

<span data-ttu-id="ff03f-115">**PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) のプロパティと同様に、このプロパティは、元のメッセージにレポートを関連付けるために使用がします。</span><span class="sxs-lookup"><span data-stu-id="ff03f-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff03f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ff03f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff03f-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ff03f-117">Protocol specifications</span></span>

<span data-ttu-id="ff03f-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff03f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff03f-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff03f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff03f-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff03f-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff03f-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ff03f-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff03f-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ff03f-122">Header files</span></span>

<span data-ttu-id="ff03f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff03f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff03f-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff03f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff03f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff03f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ff03f-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ff03f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff03f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff03f-127">See also</span></span>



[<span data-ttu-id="ff03f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff03f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff03f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff03f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff03f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ff03f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff03f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ff03f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

