---
title: PidTagRelatedMessageIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRelatedMessageIds
api_type:
- COM
ms.assetid: 51f0eb8a-0a16-4b45-9380-28caddecf955
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d909a121bdc528a04d0f400555a6f98f29da8f0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406053"
---
# <a name="pidtagrelatedmessageids-canonical-property"></a><span data-ttu-id="283b4-103">PidTagRelatedMessageIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="283b4-103">PidTagRelatedMessageIds Canonical Property</span></span>

  
  
<span data-ttu-id="283b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="283b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="283b4-105">メッセージが関連付けされているメッセージの識別子の一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="283b4-105">Contains a list of identifiers for messages to which a message is related.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="283b4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="283b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="283b4-107">PR_RELATED_IPMS</span><span class="sxs-lookup"><span data-stu-id="283b4-107">PR_RELATED_IPMS</span></span>  <br/> |
|<span data-ttu-id="283b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="283b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="283b4-109">0x002D</span><span class="sxs-lookup"><span data-stu-id="283b4-109">0x002D</span></span>  <br/> |
|<span data-ttu-id="283b4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="283b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="283b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="283b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="283b4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="283b4-112">Area:</span></span>  <br/> |<span data-ttu-id="283b4-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="283b4-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="283b4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="283b4-114">Remarks</span></span>

<span data-ttu-id="283b4-115">識別子は、プロパティ ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティで使用されるのと同PR_SEARCH_KEY特定 **の** 構築ルールを使用します。</span><span class="sxs-lookup"><span data-stu-id="283b4-115">The identifiers use the same specific construction rules as are used for the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="283b4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="283b4-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="283b4-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="283b4-117">Header files</span></span>

<span data-ttu-id="283b4-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="283b4-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="283b4-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="283b4-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="283b4-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="283b4-120">Mapitags.h</span></span>
  
> <span data-ttu-id="283b4-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="283b4-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="283b4-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="283b4-122">See also</span></span>



[<span data-ttu-id="283b4-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="283b4-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="283b4-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="283b4-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="283b4-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="283b4-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="283b4-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="283b4-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

