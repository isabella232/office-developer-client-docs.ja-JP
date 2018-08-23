---
title: PidTagMessageToken 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803000"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="74e02-103">PidTagMessageToken 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="74e02-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="74e02-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74e02-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74e02-105">メッセージを ASN.1 にセキュリティ トークンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="74e02-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74e02-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="74e02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74e02-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="74e02-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="74e02-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="74e02-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74e02-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="74e02-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="74e02-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="74e02-110">Data type:</span></span>  <br/> |<span data-ttu-id="74e02-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="74e02-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="74e02-112">領域:</span><span class="sxs-lookup"><span data-stu-id="74e02-112">Area:</span></span>  <br/> |<span data-ttu-id="74e02-113">メッセージング プロパティをセキュリティで保護します。</span><span class="sxs-lookup"><span data-stu-id="74e02-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74e02-114">注釈</span><span class="sxs-lookup"><span data-stu-id="74e02-114">Remarks</span></span>

<span data-ttu-id="74e02-115">このプロパティは、保護されているセキュリティに関連する情報の発信者から受信者を伝達します。</span><span class="sxs-lookup"><span data-stu-id="74e02-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="74e02-116">**PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) のプロパティと組み合わせて、メッセージの内容とラベルの関連付けを保証します。</span><span class="sxs-lookup"><span data-stu-id="74e02-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="74e02-117">**PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) のプロパティと組み合わせて、メッセージの内容が変更されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="74e02-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74e02-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="74e02-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="74e02-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="74e02-119">Header files</span></span>

<span data-ttu-id="74e02-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74e02-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="74e02-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="74e02-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="74e02-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74e02-122">Mapitags.h</span></span>
  
> <span data-ttu-id="74e02-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="74e02-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74e02-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="74e02-124">See also</span></span>



[<span data-ttu-id="74e02-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="74e02-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74e02-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="74e02-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74e02-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="74e02-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74e02-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="74e02-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

