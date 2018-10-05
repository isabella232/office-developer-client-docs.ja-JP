---
title: PidTagOriginalSentRepresentingAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingAddressType
api_type:
- COM
ms.assetid: 93f40161-d4e5-4ef9-a55f-cee62529fc04
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bfb768b774b1fa3d4b65ad2122f49a8ffe11a7b8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391550"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="0c6c8-103">PidTagOriginalSentRepresentingAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c6c8-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="0c6c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c6c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c6c8-105">元のメッセージが送信されたメッセージのユーザーのアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c6c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c6c8-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE、PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A、PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="0c6c8-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="0c6c8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c6c8-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="0c6c8-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="0c6c8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0c6c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c6c8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c6c8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0c6c8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-112">Area:</span></span>  <br/> |<span data-ttu-id="0c6c8-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="0c6c8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c6c8-114">備考</span><span class="sxs-lookup"><span data-stu-id="0c6c8-114">Remarks</span></span>

<span data-ttu-id="0c6c8-115">これらのプロパティは、メッセージの元の送信者に表示されるの種類です。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="0c6c8-116">会話のスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="0c6c8-117">別のクライアントの代わりにメッセージを送信するクライアント アプリケーションは、メッセージの最初の提出書類に**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) プロパティの値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="0c6c8-118">設定すると、そのことはありません変更してください。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c6c8-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0c6c8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c6c8-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0c6c8-120">Protocol specifications</span></span>

<span data-ttu-id="0c6c8-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c6c8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c6c8-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c6c8-123">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c6c8-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c6c8-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c6c8-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0c6c8-125">Header files</span></span>

<span data-ttu-id="0c6c8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c6c8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c6c8-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c6c8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0c6c8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0c6c8-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0c6c8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c6c8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c6c8-130">See also</span></span>



[<span data-ttu-id="0c6c8-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c6c8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c6c8-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c6c8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c6c8-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c6c8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c6c8-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0c6c8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

