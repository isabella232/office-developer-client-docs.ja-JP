---
title: PidTagMessageSecurityLabel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425674"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="fc852-103">PidTagMessageSecurityLabel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc852-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="fc852-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc852-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc852-105">メッセージのセキュリティ ラベルが含まれる。</span><span class="sxs-lookup"><span data-stu-id="fc852-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc852-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fc852-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc852-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="fc852-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="fc852-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fc852-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc852-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="fc852-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="fc852-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fc852-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc852-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc852-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc852-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fc852-112">Area:</span></span>  <br/> |<span data-ttu-id="fc852-113">Server</span><span class="sxs-lookup"><span data-stu-id="fc852-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc852-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fc852-114">Remarks</span></span>

<span data-ttu-id="fc852-115">このプロパティは、PR_MESSAGE_TOKEN **(** [PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) プロパティがメッセージを保護する基礎を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc852-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="fc852-116">メッセージ コンテンツとの関連付けは、トークンによって保証されます。</span><span class="sxs-lookup"><span data-stu-id="fc852-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc852-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fc852-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc852-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fc852-118">Header files</span></span>

<span data-ttu-id="fc852-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc852-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc852-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc852-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc852-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc852-121">Mapitags.h</span></span>
  
> <span data-ttu-id="fc852-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fc852-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc852-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc852-123">See also</span></span>



[<span data-ttu-id="fc852-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fc852-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc852-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc852-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc852-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fc852-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc852-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fc852-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

