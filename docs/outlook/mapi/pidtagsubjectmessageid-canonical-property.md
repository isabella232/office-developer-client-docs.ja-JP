---
title: PidTagSubjectMessageId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6b0c097616dbdc24b6e39b05aa0daaabf394e7cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803632"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a><span data-ttu-id="79bcb-103">PidTagSubjectMessageId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="79bcb-103">PidTagSubjectMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="79bcb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79bcb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79bcb-105">レポートが生成されているメッセージからコピーされたバイナリ値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="79bcb-105">Contains a binary value that is copied from the message for which a report is being generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79bcb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="79bcb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79bcb-107">PR_SUBJECT_IPM</span><span class="sxs-lookup"><span data-stu-id="79bcb-107">PR_SUBJECT_IPM</span></span>  <br/> |
|<span data-ttu-id="79bcb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="79bcb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79bcb-109">0x0038</span><span class="sxs-lookup"><span data-stu-id="79bcb-109">0x0038</span></span>  <br/> |
|<span data-ttu-id="79bcb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="79bcb-110">Data type:</span></span>  <br/> |<span data-ttu-id="79bcb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="79bcb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="79bcb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="79bcb-112">Area:</span></span>  <br/> |<span data-ttu-id="79bcb-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="79bcb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79bcb-114">備考</span><span class="sxs-lookup"><span data-stu-id="79bcb-114">Remarks</span></span>

<span data-ttu-id="79bcb-115">レポートを元のメッセージに関連付けるには、 **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) のプロパティと同様に、このプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="79bcb-115">This property, like the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property, can be used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="79bcb-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="79bcb-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="79bcb-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="79bcb-117">Header files</span></span>

<span data-ttu-id="79bcb-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79bcb-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="79bcb-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="79bcb-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="79bcb-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79bcb-120">Mapitags.h</span></span>
  
> <span data-ttu-id="79bcb-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="79bcb-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79bcb-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="79bcb-122">See also</span></span>



[<span data-ttu-id="79bcb-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="79bcb-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79bcb-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="79bcb-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79bcb-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="79bcb-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79bcb-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="79bcb-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

