---
title: PidTagRecipientCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585116"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="214e8-103">PidTagRecipientCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="214e8-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="214e8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="214e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="214e8-105">レポートで使用するため、メッセージの受信者の ASN.1 の証明書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="214e8-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="214e8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="214e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="214e8-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="214e8-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="214e8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="214e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="214e8-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="214e8-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="214e8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="214e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="214e8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="214e8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="214e8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="214e8-112">Area:</span></span>  <br/> |<span data-ttu-id="214e8-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="214e8-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="214e8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="214e8-114">Remarks</span></span>

<span data-ttu-id="214e8-115">このプロパティは、レポートで使用するための受信者の**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) のプロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="214e8-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="214e8-116">受信者が、メッセージは、配信レポートが必ずしも実際に受け取ったことを発信者に証明するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="214e8-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="214e8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="214e8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="214e8-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="214e8-118">Header files</span></span>

<span data-ttu-id="214e8-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="214e8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="214e8-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="214e8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="214e8-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="214e8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="214e8-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="214e8-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="214e8-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="214e8-123">See also</span></span>



[<span data-ttu-id="214e8-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="214e8-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="214e8-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="214e8-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="214e8-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="214e8-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="214e8-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="214e8-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

