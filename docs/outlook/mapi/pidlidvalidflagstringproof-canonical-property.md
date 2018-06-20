---
title: PidLidValidFlagStringProof の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 90f16f33e7e116e124384f9988c0c7dddaad2da5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802290"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="bd4da-103">PidLidValidFlagStringProof の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd4da-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="bd4da-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd4da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd4da-105">**DispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) プロパティの値は**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) プロパティの値を知っているエージェントによって設定されたかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd4da-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bd4da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd4da-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="bd4da-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="bd4da-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd4da-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bd4da-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bd4da-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bd4da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd4da-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="bd4da-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="bd4da-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd4da-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bd4da-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bd4da-114">領域:</span><span class="sxs-lookup"><span data-stu-id="bd4da-114">Area:</span></span>  <br/> |<span data-ttu-id="bd4da-115">タスク</span><span class="sxs-lookup"><span data-stu-id="bd4da-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd4da-116">備考</span><span class="sxs-lookup"><span data-stu-id="bd4da-116">Remarks</span></span>

<span data-ttu-id="bd4da-117">非うっかり (受信したメールやメール以外のオブジェクト)、オブジェクトの**dispidRequest**を変更する場合、クライアントは必要があります**PR_MESSAGE_DELIVERY_TIME**の値にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="bd4da-118">**PR_MESSAGE_DELIVERY_TIME**の値は、このプロパティの値が**PR_MESSAGE_DELIVERY_TIME**の値と等しい場合に、送信者が予測できない、ため、確信が**dispidRequest**の値がありませんでした。メッセージの送信者から発信します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="bd4da-119">クライアントは、クライアントの特定のセキュリティ ポリシーに従ってこの比較の結果に基づいてユーザーに**dispidRequest**の値を表示する方法を決定できます。</span><span class="sxs-lookup"><span data-stu-id="bd4da-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="bd4da-120">**DispidRequest**の値は無視する場合は**dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) の値が存在するので、このプロパティは無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd4da-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd4da-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bd4da-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd4da-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bd4da-122">Protocol specifications</span></span>

<span data-ttu-id="bd4da-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd4da-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd4da-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd4da-125">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd4da-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd4da-126">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd4da-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bd4da-127">Header files</span></span>

<span data-ttu-id="bd4da-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd4da-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd4da-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd4da-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd4da-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd4da-130">See also</span></span>



[<span data-ttu-id="bd4da-131">PidTagMessageDeliveryTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd4da-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="bd4da-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd4da-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd4da-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd4da-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd4da-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bd4da-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd4da-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bd4da-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

