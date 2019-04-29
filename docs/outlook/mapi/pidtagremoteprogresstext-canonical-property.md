---
title: PidTagRemoteProgressText 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgressText
api_type:
- COM
ms.assetid: b74d4350-4ad6-4c3f-8326-bd28537dfa0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b2a7a415f97af6aee4b9aa62b4349d2c40bfb55c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417015"
---
# <a name="pidtagremoteprogresstext-canonical-property"></a><span data-ttu-id="76003-103">PidTagRemoteProgressText 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76003-103">PidTagRemoteProgressText Canonical Property</span></span>

  
  
<span data-ttu-id="76003-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76003-105">このプロパティには、リモート転送の状態を示す文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76003-105">This property contains a string that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76003-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="76003-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76003-107">PR_REMOTE_PROGRESS_TEXT、PR_REMOTE_PROGRESS_TEXT_A、PR_REMOTE_PROGRESS_TEXT_W</span><span class="sxs-lookup"><span data-stu-id="76003-107">PR_REMOTE_PROGRESS_TEXT, PR_REMOTE_PROGRESS_TEXT_A, PR_REMOTE_PROGRESS_TEXT_W</span></span>  <br/> |
|<span data-ttu-id="76003-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="76003-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76003-109">0x3e0c</span><span class="sxs-lookup"><span data-stu-id="76003-109">0x3E0C</span></span>  <br/> |
|<span data-ttu-id="76003-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="76003-110">Data type:</span></span>  <br/> |<span data-ttu-id="76003-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76003-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76003-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="76003-112">Area:</span></span>  <br/> |<span data-ttu-id="76003-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="76003-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76003-114">注釈</span><span class="sxs-lookup"><span data-stu-id="76003-114">Remarks</span></span>

<span data-ttu-id="76003-115">このテキストに関連付けられた数値コードは、 **PR_REMOTE_PROGRESS** ([PidTagRemoteProgress](pidtagremoteprogress-canonical-property.md)) プロパティに渡されます。</span><span class="sxs-lookup"><span data-stu-id="76003-115">A numeric code associated with this text is passed in the **PR_REMOTE_PROGRESS** ([PidTagRemoteProgress](pidtagremoteprogress-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76003-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76003-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="76003-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="76003-117">Header files</span></span>

<span data-ttu-id="76003-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76003-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="76003-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76003-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="76003-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="76003-120">Mapitags.h</span></span>
  
> <span data-ttu-id="76003-121">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76003-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76003-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="76003-122">See also</span></span>



[<span data-ttu-id="76003-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="76003-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76003-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76003-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76003-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76003-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76003-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="76003-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

