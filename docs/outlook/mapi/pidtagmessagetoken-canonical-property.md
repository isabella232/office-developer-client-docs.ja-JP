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
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="66805-103">PidTagMessageToken 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66805-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="66805-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66805-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66805-105">メッセージの ASN.1 セキュリティ トークンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="66805-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66805-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66805-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66805-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="66805-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="66805-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="66805-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66805-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="66805-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="66805-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66805-110">Data type:</span></span>  <br/> |<span data-ttu-id="66805-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="66805-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="66805-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="66805-112">Area:</span></span>  <br/> |<span data-ttu-id="66805-113">セキュリティで保護されたメッセージングのプロパティ</span><span class="sxs-lookup"><span data-stu-id="66805-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66805-114">注釈</span><span class="sxs-lookup"><span data-stu-id="66805-114">Remarks</span></span>

<span data-ttu-id="66805-115">このプロパティは、保護されたセキュリティ関連の情報を発信元から受信者に伝達します。</span><span class="sxs-lookup"><span data-stu-id="66805-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="66805-116">PR_MESSAGE_SECURITY_LABEL **(** [PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) プロパティと組み合わせて、ラベルとメッセージ コンテンツとの関連付けを保証します。</span><span class="sxs-lookup"><span data-stu-id="66805-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="66805-117">このプロパティは **、PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck)](pidtagcontentintegritycheck-canonical-property.md)プロパティと組み合わせて、メッセージの内容が変更されていないか確認します。</span><span class="sxs-lookup"><span data-stu-id="66805-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66805-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66805-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="66805-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="66805-119">Header files</span></span>

<span data-ttu-id="66805-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66805-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="66805-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66805-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="66805-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66805-122">Mapitags.h</span></span>
  
> <span data-ttu-id="66805-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="66805-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66805-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="66805-124">See also</span></span>



[<span data-ttu-id="66805-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="66805-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66805-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66805-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66805-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="66805-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66805-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="66805-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

