---
title: PidTagReportTag の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c832842568ea3d64d50b56d226b66d551402ba6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803352"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="56b73-103">PidTagReportTag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="56b73-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="56b73-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56b73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56b73-105">メッセージング システムがメッセージに対して生成されたすべてのレポートをコピーする必要がありますが、バイナリのタグの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56b73-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56b73-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="56b73-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56b73-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="56b73-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="56b73-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="56b73-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56b73-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="56b73-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="56b73-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="56b73-110">Data type:</span></span>  <br/> |<span data-ttu-id="56b73-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56b73-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56b73-112">領域:</span><span class="sxs-lookup"><span data-stu-id="56b73-112">Area:</span></span>  <br/> |<span data-ttu-id="56b73-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="56b73-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56b73-114">備考</span><span class="sxs-lookup"><span data-stu-id="56b73-114">Remarks</span></span>

<span data-ttu-id="56b73-115">**PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) のプロパティと同様に、このプロパティは、元のメッセージにレポートを関連付けるために使用がします。</span><span class="sxs-lookup"><span data-stu-id="56b73-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56b73-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="56b73-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56b73-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="56b73-117">Protocol specifications</span></span>

<span data-ttu-id="56b73-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56b73-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56b73-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="56b73-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56b73-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56b73-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56b73-121">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="56b73-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56b73-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="56b73-122">Header files</span></span>

<span data-ttu-id="56b73-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56b73-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="56b73-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="56b73-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="56b73-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56b73-125">Mapitags.h</span></span>
  
> <span data-ttu-id="56b73-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="56b73-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56b73-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="56b73-127">See also</span></span>



[<span data-ttu-id="56b73-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="56b73-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56b73-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="56b73-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56b73-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="56b73-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56b73-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="56b73-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

