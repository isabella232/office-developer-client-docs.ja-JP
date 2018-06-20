---
title: PidTagRequestedDeliveryMethod の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803360"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="0b528-103">PidTagRequestedDeliveryMethod の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0b528-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="0b528-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b528-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b528-105">このプロパティには、メッセージの送信元の優先順位に従って指定の配送方法 (サービス プロバイダー) のバイナリの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b528-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b528-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0b528-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b528-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="0b528-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="0b528-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0b528-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b528-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="0b528-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="0b528-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="0b528-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b528-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b528-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b528-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0b528-112">Area:</span></span>  <br/> |<span data-ttu-id="0b528-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="0b528-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b528-114">備考</span><span class="sxs-lookup"><span data-stu-id="0b528-114">Remarks</span></span>

<span data-ttu-id="0b528-115">このに含まれている配列の各サービス プロバイダーの ASN.1 識別子のプロパティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b528-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b528-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0b528-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0b528-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0b528-117">Header files</span></span>

<span data-ttu-id="0b528-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b528-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b528-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b528-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b528-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b528-120">Mapitags.h</span></span>
  
> <span data-ttu-id="0b528-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b528-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b528-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b528-122">See also</span></span>



[<span data-ttu-id="0b528-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b528-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b528-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0b528-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b528-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="0b528-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b528-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="0b528-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

