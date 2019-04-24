---
title: PidTagRequestedDeliveryMethod 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331417"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="de6ab-103">PidTagRequestedDeliveryMethod 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de6ab-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="de6ab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de6ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de6ab-105">このプロパティには、メッセージ送信者の優先順位に従って、配信方法 (サービスプロバイダー) のバイナリ配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de6ab-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de6ab-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="de6ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de6ab-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="de6ab-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="de6ab-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="de6ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de6ab-109">0x0c18</span><span class="sxs-lookup"><span data-stu-id="de6ab-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="de6ab-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="de6ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="de6ab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="de6ab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="de6ab-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="de6ab-112">Area:</span></span>  <br/> |<span data-ttu-id="de6ab-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="de6ab-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de6ab-114">解説</span><span class="sxs-lookup"><span data-stu-id="de6ab-114">Remarks</span></span>

<span data-ttu-id="de6ab-115">このプロパティに格納されている配列は、各サービスプロバイダーの ASN で構成されています。</span><span class="sxs-lookup"><span data-stu-id="de6ab-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de6ab-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="de6ab-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="de6ab-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="de6ab-117">Header files</span></span>

<span data-ttu-id="de6ab-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de6ab-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="de6ab-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="de6ab-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="de6ab-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="de6ab-120">Mapitags.h</span></span>
  
> <span data-ttu-id="de6ab-121">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de6ab-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de6ab-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="de6ab-122">See also</span></span>



[<span data-ttu-id="de6ab-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="de6ab-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de6ab-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de6ab-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de6ab-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de6ab-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de6ab-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de6ab-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

