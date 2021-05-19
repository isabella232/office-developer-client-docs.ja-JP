---
title: PidTagContentIntegrityCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415727"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="8872c-103">PidTagContentIntegrityCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8872c-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="8872c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8872c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8872c-105">メッセージ送信者が未承認の受信者への開示からメッセージコンテンツを保護できる ASN.1 コンテンツ整合性チェック値を含む。</span><span class="sxs-lookup"><span data-stu-id="8872c-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8872c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8872c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8872c-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="8872c-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="8872c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8872c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8872c-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="8872c-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="8872c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8872c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8872c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8872c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8872c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8872c-112">Area:</span></span>  <br/> |<span data-ttu-id="8872c-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8872c-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8872c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8872c-114">Remarks</span></span>

<span data-ttu-id="8872c-115">このプロパティは、メッセージ コンテンツの否認不可を提供します。</span><span class="sxs-lookup"><span data-stu-id="8872c-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="8872c-116">メッセージ **のPR_MESSAGE_TOKEN** [(PidTagMessageToken)](pidtagmessagetoken-canonical-property.md)と組み合わせて、メッセージの内容が変更されずに宛先に到着します。</span><span class="sxs-lookup"><span data-stu-id="8872c-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8872c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8872c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8872c-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8872c-118">Header files</span></span>

<span data-ttu-id="8872c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8872c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8872c-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8872c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8872c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8872c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8872c-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8872c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8872c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8872c-123">See also</span></span>



[<span data-ttu-id="8872c-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8872c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8872c-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8872c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8872c-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8872c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8872c-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8872c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

