---
title: PidLidValidFlagStringProof 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315387"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="ed7d8-103">PidLidValidFlagStringProof 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed7d8-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="ed7d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed7d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed7d8-105">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) プロパティの値を知っているエージェントによって、 **dispidrequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) プロパティの値が設定されているかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed7d8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ed7d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed7d8-107">dispidvalidflagstringproof</span><span class="sxs-lookup"><span data-stu-id="ed7d8-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="ed7d8-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="ed7d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed7d8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ed7d8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ed7d8-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ed7d8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed7d8-111">0x000085bf</span><span class="sxs-lookup"><span data-stu-id="ed7d8-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="ed7d8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ed7d8-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed7d8-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ed7d8-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ed7d8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="ed7d8-114">Area:</span></span>  <br/> |<span data-ttu-id="ed7d8-115">タスク</span><span class="sxs-lookup"><span data-stu-id="ed7d8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed7d8-116">解説</span><span class="sxs-lookup"><span data-stu-id="ed7d8-116">Remarks</span></span>

<span data-ttu-id="ed7d8-117">送信可能以外のオブジェクト (受信メールオブジェクトとメール以外のオブジェクト) では、 **dispidrequest**を変更するときに、クライアントはこの値を**PR_MESSAGE_DELIVERY_TIME**の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="ed7d8-118">**PR_MESSAGE_DELIVERY_TIME**の値を送信者が予測することはできないため、このプロパティの値が**PR_MESSAGE_DELIVERY_TIME**の値と等しい場合、 **dispidrequest**の値が次の値でないことが合理的であることを示します。メッセージの送信者から発信されます。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="ed7d8-119">クライアントは、クライアントの特定のセキュリティポリシーに従って、この比較の結果に基づいて、 **dispidrequest**の値をエンドユーザーに提示する方法を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="ed7d8-120">**dispidflagstringenum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) の値が存在するために**dispidrequest**の値が無視される場合、このプロパティは無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed7d8-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed7d8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed7d8-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ed7d8-122">Protocol specifications</span></span>

<span data-ttu-id="ed7d8-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed7d8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed7d8-124">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed7d8-125">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed7d8-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed7d8-126">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed7d8-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ed7d8-127">Header files</span></span>

<span data-ttu-id="ed7d8-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed7d8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed7d8-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed7d8-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed7d8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed7d8-130">See also</span></span>



[<span data-ttu-id="ed7d8-131">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed7d8-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="ed7d8-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ed7d8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed7d8-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed7d8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed7d8-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ed7d8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed7d8-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ed7d8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

