---
title: PidTagReceivedByAddressType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 96a53e427460990983242009500ade9ae0c5ada5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803244"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="4f7bb-103">PidTagReceivedByAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4f7bb-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="4f7bb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f7bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f7bb-105">電子メール アドレスの種類、SMTP など、メッセージング ユーザーに実際にメッセージが表示されますが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f7bb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f7bb-107">PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="4f7bb-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="4f7bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4f7bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f7bb-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="4f7bb-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="4f7bb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f7bb-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4f7bb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4f7bb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4f7bb-112">Area:</span></span>  <br/> |<span data-ttu-id="4f7bb-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="4f7bb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f7bb-114">備考</span><span class="sxs-lookup"><span data-stu-id="4f7bb-114">Remarks</span></span>

<span data-ttu-id="4f7bb-115">これらのプロパティでは、実際にメッセージを受信するメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="4f7bb-116">着信トランスポート プロバイダーが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="4f7bb-117">アドレスの種類の文字列には、のみ、大文字のアルファベット文字 A から Z、および 0 から 9 までの番号を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="4f7bb-118">これらのプロパティは、アドレスの構築方法を示すため、SMTP などのアドレスの種類を指定することによって、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) のプロパティを修飾します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f7bb-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4f7bb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f7bb-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4f7bb-120">Protocol specifications</span></span>

<span data-ttu-id="4f7bb-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f7bb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f7bb-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f7bb-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f7bb-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f7bb-124">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f7bb-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4f7bb-125">Header files</span></span>

<span data-ttu-id="4f7bb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f7bb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f7bb-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f7bb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f7bb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4f7bb-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f7bb-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f7bb-130">See also</span></span>



[<span data-ttu-id="4f7bb-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f7bb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f7bb-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4f7bb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f7bb-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4f7bb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f7bb-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4f7bb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

