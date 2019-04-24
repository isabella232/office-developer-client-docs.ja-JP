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
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315422"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="90e8d-103">PidLidUseTnef 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90e8d-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="90e8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90e8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90e8d-105">メッセージが MAPI から多目的のインターネットメール内線 (MIME) または簡易メール転送プロトコル (SMTP) 形式に変換されたときに、メッセージにトランスポートニュートラルカプセル化形式 (TNEF) を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="90e8d-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90e8d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="90e8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90e8d-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="90e8d-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="90e8d-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="90e8d-108">Property set:</span></span>  <br/> |<span data-ttu-id="90e8d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="90e8d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="90e8d-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="90e8d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="90e8d-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="90e8d-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="90e8d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="90e8d-112">Data type:</span></span>  <br/> |<span data-ttu-id="90e8d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="90e8d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="90e8d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="90e8d-114">Area:</span></span>  <br/> |<span data-ttu-id="90e8d-115">実行時の構成</span><span class="sxs-lookup"><span data-stu-id="90e8d-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90e8d-116">解説</span><span class="sxs-lookup"><span data-stu-id="90e8d-116">Remarks</span></span>

<span data-ttu-id="90e8d-117">このプロパティは、メッセージが tnef から MIME または SMTP 形式に変換されたときに、メッセージに tnef を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="90e8d-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="90e8d-118">このプロパティは存在しない場合があり、その場合は TNEF をメッセージに含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="90e8d-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="90e8d-119">このプロパティは、メッセージが POP3/SMTP メールアカウントから送信され、メッセージが他のプロバイダー (Microsoft Exchange Server など) によって送信されたときには適用されない場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="90e8d-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="90e8d-120">投票ボタンが有効になっている場合や、OLE 埋め込みオブジェクトがメッセージに添付されている場合など、特定の状況では、Outlook でこのプロパティを設定して TNEF の使用を強制することができます。</span><span class="sxs-lookup"><span data-stu-id="90e8d-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="90e8d-121">**PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) プロパティを使用して、メッセージを送信するときに、TNEF ではなくプレーンテキストのみを適用できます。</span><span class="sxs-lookup"><span data-stu-id="90e8d-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="90e8d-122">**PidLidUseTNEF**は**PR_MSG_EDITOR_FORMAT**の設定よりも優先されるので、送信メッセージにプレーンテキストを強制するアプリケーションは、 **PidLidUseTNEF**を検索して FALSE にリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e8d-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="90e8d-123">さらに、このアドインでは、TNEF を必要とするメッセージ機能を削除して、最終的に送信されるメッセージの添付ファイルを使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90e8d-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="90e8d-124">[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出して、 **CCSF_USE_TNEF**フラグを使用して、送信 MAPI メッセージを MIME ストリームに変換することにより、TNEF を強制することもできます。</span><span class="sxs-lookup"><span data-stu-id="90e8d-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="90e8d-125">これは、 **PidLidUseTNEF**が設定されていない場合でも適用されます。</span><span class="sxs-lookup"><span data-stu-id="90e8d-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90e8d-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90e8d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90e8d-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="90e8d-127">Protocol specifications</span></span>

<span data-ttu-id="90e8d-128">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90e8d-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90e8d-129">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="90e8d-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90e8d-130">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90e8d-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90e8d-131">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="90e8d-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="90e8d-132">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90e8d-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90e8d-133">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="90e8d-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90e8d-134">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="90e8d-134">Header files</span></span>

<span data-ttu-id="90e8d-135">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90e8d-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="90e8d-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90e8d-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90e8d-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="90e8d-137">See also</span></span>



[<span data-ttu-id="90e8d-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="90e8d-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90e8d-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90e8d-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90e8d-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90e8d-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90e8d-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90e8d-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

