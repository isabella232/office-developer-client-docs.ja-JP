---
title: PidLidUseTnef 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0d5588218fd74f005de19daba002cd622c13a17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587188"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="474ad-103">PidLidUseTnef 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="474ad-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="474ad-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="474ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="474ad-105">トランスポート ニュートラル カプセル化形式 (TNEF) をそのメッセージは MAPI から多目的インターネット メール拡張 (MIME) または簡易メール転送プロトコル (SMTP) の形式に変換するとメッセージに含める必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="474ad-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="474ad-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="474ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="474ad-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="474ad-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="474ad-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="474ad-108">Property set:</span></span>  <br/> |<span data-ttu-id="474ad-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="474ad-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="474ad-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="474ad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="474ad-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="474ad-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="474ad-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="474ad-112">Data type:</span></span>  <br/> |<span data-ttu-id="474ad-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="474ad-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="474ad-114">領域:</span><span class="sxs-lookup"><span data-stu-id="474ad-114">Area:</span></span>  <br/> |<span data-ttu-id="474ad-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="474ad-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="474ad-116">注釈</span><span class="sxs-lookup"><span data-stu-id="474ad-116">Remarks</span></span>

<span data-ttu-id="474ad-117">このプロパティでは、TNEF をメッセージには TNEF から MIME または SMTP 形式に変換するとメッセージに含める必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="474ad-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="474ad-118">このプロパティが失われている可能性があり、メッセージの TNEF を含めない場合は、します。</span><span class="sxs-lookup"><span data-stu-id="474ad-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="474ad-119">このプロパティは、メッセージが POP3 または SMTP のメール アカウントから送信され、Microsoft Exchange Server など、他のプロバイダーによって、メッセージが送信されるときは適用されませんがある場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="474ad-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="474ad-120">状況によっては、オブジェクトがメッセージに接続されているボタンが有効になっている場合や OLE 埋め込みを返信するときなど、Outlook プロパティを設定この TNEF の使用を強制します。</span><span class="sxs-lookup"><span data-stu-id="474ad-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="474ad-121">メッセージを送信するときに、プレーン テキストと、TNEF ではないだけを適用するのには、 **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="474ad-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="474ad-122">**PidLidUseTNEF**は、 **PR_MSG_EDITOR_FORMAT**の設定をオーバーライドするため送信メッセージのテキスト形式を強制的にしようとしているアプリケーション必要がありますもの**PidLidUseTNEF**を FALSE にリセットします。</span><span class="sxs-lookup"><span data-stu-id="474ad-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="474ad-123">さらに、アドインは、最後に送信されるメッセージに添付ファイルを使用できなくなるを避けるために tnef メッセージ機能を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="474ad-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="474ad-124">使用中の MAPI メッセージを MIME ストリームに変換する[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出すときに**CCSF_USE_TNEF**フラグは、TNEF にも適用できます。</span><span class="sxs-lookup"><span data-stu-id="474ad-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="474ad-125">これは、 **PidLidUseTNEF**が設定されていない場合でも適用されます。</span><span class="sxs-lookup"><span data-stu-id="474ad-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="474ad-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="474ad-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="474ad-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="474ad-127">Protocol specifications</span></span>

<span data-ttu-id="474ad-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="474ad-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="474ad-129">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="474ad-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="474ad-130">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="474ad-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="474ad-131">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="474ad-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="474ad-132">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="474ad-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="474ad-133">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="474ad-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="474ad-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="474ad-134">Header files</span></span>

<span data-ttu-id="474ad-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="474ad-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="474ad-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="474ad-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="474ad-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="474ad-137">See also</span></span>



[<span data-ttu-id="474ad-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="474ad-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="474ad-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="474ad-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="474ad-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="474ad-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="474ad-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="474ad-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

