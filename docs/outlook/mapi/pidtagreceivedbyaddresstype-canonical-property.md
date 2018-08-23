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
ms.openlocfilehash: cd7a287a2240d372edf6cca6bac522266c0ca620
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581168"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="7d183-103">PidTagReceivedByAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d183-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="7d183-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d183-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d183-105">電子メール アドレスの種類、SMTP など、メッセージング ユーザーに実際にメッセージが表示されますが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d183-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d183-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7d183-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d183-107">PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="7d183-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="7d183-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7d183-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d183-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="7d183-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="7d183-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7d183-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d183-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d183-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7d183-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7d183-112">Area:</span></span>  <br/> |<span data-ttu-id="7d183-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="7d183-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d183-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7d183-114">Remarks</span></span>

<span data-ttu-id="7d183-115">これらのプロパティでは、実際にメッセージを受信するメッセージング ユーザーのアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="7d183-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="7d183-116">着信トランスポート プロバイダーが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7d183-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="7d183-117">アドレスの種類の文字列には、のみ、大文字のアルファベット文字 A から Z、および 0 から 9 までの番号を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7d183-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="7d183-118">これらのプロパティは、アドレスの構築方法を示すため、SMTP などのアドレスの種類を指定することによって、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) のプロパティを修飾します。</span><span class="sxs-lookup"><span data-stu-id="7d183-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d183-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7d183-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d183-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7d183-120">Protocol specifications</span></span>

<span data-ttu-id="7d183-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d183-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d183-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d183-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d183-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d183-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d183-124">プロパティは、電子メール メッセージの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d183-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d183-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7d183-125">Header files</span></span>

<span data-ttu-id="7d183-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d183-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d183-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d183-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d183-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d183-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7d183-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d183-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d183-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d183-130">See also</span></span>



[<span data-ttu-id="7d183-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d183-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d183-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d183-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d183-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7d183-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d183-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7d183-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

