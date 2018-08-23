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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a6caa322e1d266be1fe56aecd89736e757067758
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594370"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="cf9b4-103">PidTagMessageSecurityLabel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf9b4-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="cf9b4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf9b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf9b4-105">メッセージのセキュリティ ラベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf9b4-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf9b4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cf9b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf9b4-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="cf9b4-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="cf9b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cf9b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf9b4-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="cf9b4-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="cf9b4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cf9b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf9b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cf9b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cf9b4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cf9b4-112">Area:</span></span>  <br/> |<span data-ttu-id="cf9b4-113">Server</span><span class="sxs-lookup"><span data-stu-id="cf9b4-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf9b4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cf9b4-114">Remarks</span></span>

<span data-ttu-id="cf9b4-115">このプロパティは、 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) のプロパティがメッセージを保護する基盤を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf9b4-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="cf9b4-116">トークンでは、メッセージの内容との関連が保証されます。</span><span class="sxs-lookup"><span data-stu-id="cf9b4-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf9b4-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cf9b4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cf9b4-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cf9b4-118">Header files</span></span>

<span data-ttu-id="cf9b4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf9b4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf9b4-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf9b4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf9b4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf9b4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cf9b4-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf9b4-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf9b4-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf9b4-123">See also</span></span>



[<span data-ttu-id="cf9b4-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf9b4-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf9b4-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf9b4-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf9b4-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cf9b4-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf9b4-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cf9b4-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

