---
title: PidTagObsoletedMessageIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObsoletedMessageIds
api_type:
- HeaderDef
ms.assetid: bc979398-f1ad-4496-b982-428b95719369
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f00a57798b03edb368fb0dc59fead7a2e9f5c8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329247"
---
# <a name="pidtagobsoletedmessageids-canonical-property"></a><span data-ttu-id="5392f-103">PidTagObsoletedMessageIds 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5392f-103">PidTagObsoletedMessageIds Canonical Property</span></span>

  
  
<span data-ttu-id="5392f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5392f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5392f-105">このメッセージが優先するメッセージの識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="5392f-105">Contains the identifiers of messages that this message supersedes.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5392f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5392f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5392f-107">PR_OBSOLETED_IPMS</span><span class="sxs-lookup"><span data-stu-id="5392f-107">PR_OBSOLETED_IPMS</span></span>  <br/> |
|<span data-ttu-id="5392f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5392f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5392f-109">0x001f</span><span class="sxs-lookup"><span data-stu-id="5392f-109">0x001F</span></span>  <br/> |
|<span data-ttu-id="5392f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5392f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5392f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5392f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5392f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5392f-112">Area:</span></span>  <br/> |<span data-ttu-id="5392f-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="5392f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5392f-114">解説</span><span class="sxs-lookup"><span data-stu-id="5392f-114">Remarks</span></span>

<span data-ttu-id="5392f-115">このプロパティに含まれる識別子は、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの形式を使用する標準の検索キーです。</span><span class="sxs-lookup"><span data-stu-id="5392f-115">The identifiers contained in this property are standard search keys using the format of the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5392f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5392f-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5392f-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5392f-117">Header files</span></span>

<span data-ttu-id="5392f-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5392f-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5392f-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5392f-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5392f-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="5392f-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5392f-121">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5392f-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5392f-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="5392f-122">See also</span></span>



[<span data-ttu-id="5392f-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5392f-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5392f-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5392f-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5392f-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5392f-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5392f-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5392f-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

