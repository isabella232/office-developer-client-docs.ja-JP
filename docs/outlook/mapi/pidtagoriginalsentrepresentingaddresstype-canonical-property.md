---
title: PidTagOriginalSentRepresentingAddressType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7fcd358b2ada5137ed28f4439dcc9d4ebdc50305
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803076"
---
# <a name="pidtagoriginalsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="9201e-103">PidTagOriginalSentRepresentingAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9201e-103">PidTagOriginalSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="9201e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9201e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9201e-105">元のメッセージが送信されたメッセージのユーザーのアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9201e-105">Contains the address type of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9201e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9201e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9201e-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE、PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A、PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="9201e-107">PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_A, PR_ORIGINAL_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="9201e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9201e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9201e-109">0x0068</span><span class="sxs-lookup"><span data-stu-id="9201e-109">0x0068</span></span>  <br/> |
|<span data-ttu-id="9201e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9201e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9201e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9201e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9201e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9201e-112">Area:</span></span>  <br/> |<span data-ttu-id="9201e-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="9201e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9201e-114">備考</span><span class="sxs-lookup"><span data-stu-id="9201e-114">Remarks</span></span>

<span data-ttu-id="9201e-115">これらのプロパティは、メッセージの元の送信者に表示されるの種類です。</span><span class="sxs-lookup"><span data-stu-id="9201e-115">These properties are the type for the original represented sender of a message.</span></span> <span data-ttu-id="9201e-116">会話のスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9201e-116">They are used in a conversation thread.</span></span>
  
<span data-ttu-id="9201e-117">別のクライアントの代わりにメッセージを送信するクライアント アプリケーションは、メッセージの最初の提出書類に**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) プロパティの値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9201e-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="9201e-118">設定すると、そのことはありません変更してください。</span><span class="sxs-lookup"><span data-stu-id="9201e-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9201e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9201e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9201e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9201e-120">Protocol specifications</span></span>

<span data-ttu-id="9201e-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9201e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9201e-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9201e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9201e-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9201e-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9201e-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9201e-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9201e-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9201e-125">Header files</span></span>

<span data-ttu-id="9201e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9201e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9201e-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9201e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9201e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9201e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9201e-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9201e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9201e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="9201e-130">See also</span></span>



[<span data-ttu-id="9201e-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9201e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9201e-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9201e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9201e-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9201e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9201e-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9201e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

