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
# <a name="pidtagcontentreturnrequested-canonical-property"></a><span data-ttu-id="eaad0-103">PidTagContentReturnRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eaad0-103">PidTagContentReturnRequested Canonical Property</span></span>

  
  
<span data-ttu-id="eaad0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaad0-105">メッセージが配信不能レポートと共に返される必要がある場合は、TRUE を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaad0-105">Contains TRUE if a message should be returned with a nondelivery report.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eaad0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eaad0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eaad0-107">PR_CONTENT_RETURN_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="eaad0-107">PR_CONTENT_RETURN_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="eaad0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eaad0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eaad0-109">0x000a</span><span class="sxs-lookup"><span data-stu-id="eaad0-109">0x000A</span></span>  <br/> |
|<span data-ttu-id="eaad0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eaad0-110">Data type:</span></span>  <br/> |<span data-ttu-id="eaad0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eaad0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eaad0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eaad0-112">Area:</span></span>  <br/> |<span data-ttu-id="eaad0-113">レポート</span><span class="sxs-lookup"><span data-stu-id="eaad0-113">Report</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaad0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="eaad0-114">Remarks</span></span>

<span data-ttu-id="eaad0-115">このプロパティが設定されていない場合、MAPI は TRUE の値を持つものとして扱います。</span><span class="sxs-lookup"><span data-stu-id="eaad0-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eaad0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eaad0-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eaad0-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="eaad0-117">Header files</span></span>

<span data-ttu-id="eaad0-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaad0-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="eaad0-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eaad0-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="eaad0-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="eaad0-120">Mapitags.h</span></span>
  
> <span data-ttu-id="eaad0-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eaad0-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eaad0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaad0-122">See also</span></span>



[<span data-ttu-id="eaad0-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eaad0-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eaad0-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eaad0-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eaad0-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eaad0-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eaad0-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eaad0-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

