---
title: PidTagReceivedByAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359228"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="30d78-103">PidTagReceivedByAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="30d78-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="30d78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30d78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30d78-105">実際にメッセージを受信するメッセージングユーザーの電子メールアドレスの種類 (SMTP など) を格納します。</span><span class="sxs-lookup"><span data-stu-id="30d78-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30d78-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="30d78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30d78-107">PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="30d78-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="30d78-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="30d78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30d78-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="30d78-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="30d78-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="30d78-110">Data type:</span></span>  <br/> |<span data-ttu-id="30d78-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30d78-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="30d78-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="30d78-112">Area:</span></span>  <br/> |<span data-ttu-id="30d78-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="30d78-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30d78-114">解説</span><span class="sxs-lookup"><span data-stu-id="30d78-114">Remarks</span></span>

<span data-ttu-id="30d78-115">これらのプロパティは、実際にメッセージを受信するメッセージングユーザーのアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="30d78-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="30d78-116">これらは、受信トランスポートプロバイダーによって設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="30d78-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="30d78-117">アドレスの種類の文字列には、a ~ Z の英字と 0 ~ 9 の数字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="30d78-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="30d78-118">これらのプロパティは、SMTP などのアドレスの種類を指定することによって、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) プロパティを修飾し、アドレスの構築方法を示します。</span><span class="sxs-lookup"><span data-stu-id="30d78-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30d78-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="30d78-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30d78-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="30d78-120">Protocol specifications</span></span>

<span data-ttu-id="30d78-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30d78-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30d78-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="30d78-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30d78-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30d78-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30d78-124">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="30d78-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30d78-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="30d78-125">Header files</span></span>

<span data-ttu-id="30d78-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30d78-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="30d78-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="30d78-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="30d78-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="30d78-128">Mapitags.h</span></span>
  
> <span data-ttu-id="30d78-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="30d78-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30d78-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="30d78-130">See also</span></span>



[<span data-ttu-id="30d78-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="30d78-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30d78-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="30d78-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30d78-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="30d78-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30d78-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="30d78-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

