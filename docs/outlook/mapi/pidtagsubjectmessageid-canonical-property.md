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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7bd5a030d11577c2afabb8a2253cf4f6129814cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407103"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a><span data-ttu-id="be5c0-103">PidTagSubjectMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="be5c0-103">PidTagSubjectMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="be5c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be5c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be5c0-105">レポートが生成されるメッセージからコピーされるバイナリ値を含む。</span><span class="sxs-lookup"><span data-stu-id="be5c0-105">Contains a binary value that is copied from the message for which a report is being generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be5c0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="be5c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be5c0-107">PR_SUBJECT_IPM</span><span class="sxs-lookup"><span data-stu-id="be5c0-107">PR_SUBJECT_IPM</span></span>  <br/> |
|<span data-ttu-id="be5c0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="be5c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be5c0-109">0x0038</span><span class="sxs-lookup"><span data-stu-id="be5c0-109">0x0038</span></span>  <br/> |
|<span data-ttu-id="be5c0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="be5c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="be5c0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be5c0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be5c0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="be5c0-112">Area:</span></span>  <br/> |<span data-ttu-id="be5c0-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="be5c0-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be5c0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="be5c0-114">Remarks</span></span>

<span data-ttu-id="be5c0-115">このプロパティは **、PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) プロパティと同様に、レポートを元のメッセージと関連付ける場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="be5c0-115">This property, like the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property, can be used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be5c0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="be5c0-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="be5c0-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="be5c0-117">Header files</span></span>

<span data-ttu-id="be5c0-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be5c0-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="be5c0-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="be5c0-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="be5c0-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be5c0-120">Mapitags.h</span></span>
  
> <span data-ttu-id="be5c0-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="be5c0-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be5c0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="be5c0-122">See also</span></span>



[<span data-ttu-id="be5c0-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="be5c0-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be5c0-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="be5c0-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be5c0-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="be5c0-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be5c0-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="be5c0-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

