---
title: PidTagClientSubmitTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345718"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="c85d3-103">PidTagClientSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85d3-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="c85d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c85d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c85d3-105">メッセージ送信者がメッセージを送信した日時を格納します。</span><span class="sxs-lookup"><span data-stu-id="c85d3-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c85d3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c85d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c85d3-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="c85d3-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="c85d3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c85d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c85d3-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="c85d3-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="c85d3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c85d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c85d3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c85d3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c85d3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c85d3-112">Area:</span></span>  <br/> |<span data-ttu-id="c85d3-113">メッセージ時刻</span><span class="sxs-lookup"><span data-stu-id="c85d3-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c85d3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c85d3-114">Remarks</span></span>

<span data-ttu-id="c85d3-115">ストア プロバイダーは **、PR_CLIENT_SUBMIT_TIME** アプリケーションが [IMessage::SubmitMessage](imessage-submitmessage.md)と呼ばれる時刻に設定します。</span><span class="sxs-lookup"><span data-stu-id="c85d3-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c85d3-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c85d3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c85d3-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c85d3-117">Protocol specifications</span></span>

<span data-ttu-id="c85d3-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85d3-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85d3-119">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c85d3-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c85d3-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c85d3-120">Header files</span></span>

<span data-ttu-id="c85d3-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c85d3-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c85d3-122">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c85d3-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c85d3-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c85d3-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c85d3-124">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c85d3-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c85d3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="c85d3-125">See also</span></span>



[<span data-ttu-id="c85d3-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c85d3-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c85d3-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c85d3-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c85d3-128">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c85d3-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c85d3-129">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c85d3-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

