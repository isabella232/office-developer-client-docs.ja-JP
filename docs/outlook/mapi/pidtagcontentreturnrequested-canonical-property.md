---
title: PidTagContentReturnRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentReturnRequested
api_type:
- HeaderDef
ms.assetid: f86f7c59-42ab-4ac0-80fe-c985103e6bd6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c64288f393f15ee330065a43a92930f2e6f4e134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419773"
---
# <a name="pidtagcontentreturnrequested-canonical-property"></a><span data-ttu-id="e8e29-103">PidTagContentReturnRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8e29-103">PidTagContentReturnRequested Canonical Property</span></span>

  
  
<span data-ttu-id="e8e29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8e29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8e29-105">メッセージを非送信レポートと一緒に返す必要がある場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="e8e29-105">Contains TRUE if a message should be returned with a nondelivery report.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8e29-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e8e29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8e29-107">PR_CONTENT_RETURN_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="e8e29-107">PR_CONTENT_RETURN_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="e8e29-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e8e29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8e29-109">0x000A</span><span class="sxs-lookup"><span data-stu-id="e8e29-109">0x000A</span></span>  <br/> |
|<span data-ttu-id="e8e29-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e8e29-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8e29-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e8e29-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e8e29-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e8e29-112">Area:</span></span>  <br/> |<span data-ttu-id="e8e29-113">レポート</span><span class="sxs-lookup"><span data-stu-id="e8e29-113">Report</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8e29-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e8e29-114">Remarks</span></span>

<span data-ttu-id="e8e29-115">このプロパティが設定されていない場合、MAPI は TRUE 値を持つプロパティとして扱います。</span><span class="sxs-lookup"><span data-stu-id="e8e29-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e8e29-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e8e29-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8e29-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e8e29-117">Header files</span></span>

<span data-ttu-id="e8e29-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8e29-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8e29-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8e29-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8e29-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e8e29-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e8e29-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e8e29-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8e29-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8e29-122">See also</span></span>



[<span data-ttu-id="e8e29-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e8e29-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8e29-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8e29-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8e29-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e8e29-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8e29-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e8e29-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

