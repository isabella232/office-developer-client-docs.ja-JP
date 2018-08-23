---
title: PidTagSubjectMessageId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c89a0a86ac733cd2cce1efc071e47fcb011fec18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573069"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a><span data-ttu-id="f6329-103">PidTagSubjectMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6329-103">PidTagSubjectMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="f6329-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6329-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6329-105">レポートが生成されているメッセージからコピーされたバイナリ値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6329-105">Contains a binary value that is copied from the message for which a report is being generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6329-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f6329-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6329-107">PR_SUBJECT_IPM</span><span class="sxs-lookup"><span data-stu-id="f6329-107">PR_SUBJECT_IPM</span></span>  <br/> |
|<span data-ttu-id="f6329-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f6329-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6329-109">0x0038</span><span class="sxs-lookup"><span data-stu-id="f6329-109">0x0038</span></span>  <br/> |
|<span data-ttu-id="f6329-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f6329-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6329-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6329-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6329-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f6329-112">Area:</span></span>  <br/> |<span data-ttu-id="f6329-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="f6329-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6329-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f6329-114">Remarks</span></span>

<span data-ttu-id="f6329-115">レポートを元のメッセージに関連付けるには、 **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) のプロパティと同様に、このプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6329-115">This property, like the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property, can be used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f6329-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f6329-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f6329-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f6329-117">Header files</span></span>

<span data-ttu-id="f6329-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6329-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6329-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6329-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6329-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6329-120">Mapitags.h</span></span>
  
> <span data-ttu-id="f6329-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6329-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6329-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6329-122">See also</span></span>



[<span data-ttu-id="f6329-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6329-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6329-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6329-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6329-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f6329-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6329-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f6329-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

