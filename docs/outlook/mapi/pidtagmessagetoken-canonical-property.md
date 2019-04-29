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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408188"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="0fbad-103">PidTagMessageToken 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0fbad-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="0fbad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fbad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fbad-105">メッセージの ASN. 1 セキュリティトークンが格納されています。</span><span class="sxs-lookup"><span data-stu-id="0fbad-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fbad-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0fbad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fbad-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="0fbad-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="0fbad-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0fbad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0fbad-109">0x0c03</span><span class="sxs-lookup"><span data-stu-id="0fbad-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="0fbad-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0fbad-110">Data type:</span></span>  <br/> |<span data-ttu-id="0fbad-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0fbad-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0fbad-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0fbad-112">Area:</span></span>  <br/> |<span data-ttu-id="0fbad-113">セキュリティで保護されたメッセージングのプロパティ</span><span class="sxs-lookup"><span data-stu-id="0fbad-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fbad-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0fbad-114">Remarks</span></span>

<span data-ttu-id="0fbad-115">このプロパティは、保護されたセキュリティ関連の情報を発信者から受信者に伝達します。</span><span class="sxs-lookup"><span data-stu-id="0fbad-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="0fbad-116">**PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) プロパティと共に、ラベルがメッセージの内容と関連付けられていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="0fbad-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="0fbad-117">**PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) プロパティと共に、メッセージの内容が変更されていないかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0fbad-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fbad-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0fbad-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0fbad-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0fbad-119">Header files</span></span>

<span data-ttu-id="0fbad-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fbad-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fbad-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0fbad-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="0fbad-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0fbad-122">Mapitags.h</span></span>
  
> <span data-ttu-id="0fbad-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fbad-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fbad-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fbad-124">See also</span></span>



[<span data-ttu-id="0fbad-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0fbad-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fbad-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0fbad-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fbad-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0fbad-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fbad-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0fbad-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

