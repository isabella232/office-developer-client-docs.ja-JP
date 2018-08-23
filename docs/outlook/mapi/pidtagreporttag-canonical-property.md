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
ms.openlocfilehash: c832842568ea3d64d50b56d226b66d551402ba6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803352"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="df660-103">PidTagReportTag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="df660-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="df660-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df660-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df660-105">メッセージング システムがメッセージに対して生成されたすべてのレポートをコピーする必要がありますが、バイナリのタグの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df660-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df660-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="df660-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df660-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="df660-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="df660-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="df660-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df660-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="df660-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="df660-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="df660-110">Data type:</span></span>  <br/> |<span data-ttu-id="df660-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df660-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df660-112">領域:</span><span class="sxs-lookup"><span data-stu-id="df660-112">Area:</span></span>  <br/> |<span data-ttu-id="df660-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="df660-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df660-114">注釈</span><span class="sxs-lookup"><span data-stu-id="df660-114">Remarks</span></span>

<span data-ttu-id="df660-115">**PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) のプロパティと同様に、このプロパティは、元のメッセージにレポートを関連付けるために使用がします。</span><span class="sxs-lookup"><span data-stu-id="df660-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df660-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="df660-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df660-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="df660-117">Protocol specifications</span></span>

<span data-ttu-id="df660-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df660-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df660-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="df660-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df660-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df660-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df660-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="df660-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df660-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="df660-122">Header files</span></span>

<span data-ttu-id="df660-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df660-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="df660-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="df660-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="df660-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df660-125">Mapitags.h</span></span>
  
> <span data-ttu-id="df660-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df660-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df660-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="df660-127">See also</span></span>



[<span data-ttu-id="df660-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="df660-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df660-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="df660-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df660-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="df660-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df660-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="df660-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

