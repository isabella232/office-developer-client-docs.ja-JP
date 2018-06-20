---
title: PidTagRecipientCertificate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803286"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="586f2-103">PidTagRecipientCertificate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="586f2-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="586f2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="586f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="586f2-105">レポートで使用するため、メッセージの受信者の ASN.1 の証明書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="586f2-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="586f2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="586f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="586f2-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="586f2-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="586f2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="586f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="586f2-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="586f2-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="586f2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="586f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="586f2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="586f2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="586f2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="586f2-112">Area:</span></span>  <br/> |<span data-ttu-id="586f2-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="586f2-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="586f2-114">備考</span><span class="sxs-lookup"><span data-stu-id="586f2-114">Remarks</span></span>

<span data-ttu-id="586f2-115">このプロパティは、レポートで使用するための受信者の**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) のプロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="586f2-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="586f2-116">受信者が、メッセージは、配信レポートが必ずしも実際に受け取ったことを発信者に証明するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="586f2-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="586f2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="586f2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="586f2-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="586f2-118">Header files</span></span>

<span data-ttu-id="586f2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="586f2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="586f2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="586f2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="586f2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="586f2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="586f2-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="586f2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="586f2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="586f2-123">See also</span></span>



[<span data-ttu-id="586f2-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="586f2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="586f2-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="586f2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="586f2-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="586f2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="586f2-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="586f2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

