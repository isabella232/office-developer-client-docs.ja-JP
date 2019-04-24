---
title: PidTagMessageRecipientMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325621"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="de274-103">PidTagMessageRecipientMe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de274-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="de274-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de274-105">このメッセージのユーザーが、このメッセージのプライマリ (宛先)、カーボンコピー (CC)、または bcc (ブラインドカーボンコピー) の受信者として指定されていて、配布リストの一部ではない場合は、TRUE を指定します。</span><span class="sxs-lookup"><span data-stu-id="de274-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de274-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="de274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de274-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="de274-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="de274-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="de274-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de274-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="de274-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="de274-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="de274-110">Data type:</span></span>  <br/> |<span data-ttu-id="de274-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="de274-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="de274-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="de274-112">Area:</span></span>  <br/> |<span data-ttu-id="de274-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="de274-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de274-114">解説</span><span class="sxs-lookup"><span data-stu-id="de274-114">Remarks</span></span>

<span data-ttu-id="de274-115">このプロパティを使用すると、リスト内のすべてのエントリを調査することなく、ユーザー名が受信者リスト内で明示的に表示されるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="de274-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="de274-116">この値は、 **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) および**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) のプロパティの論理**OR**操作、および BCC 情報 (それ以外の場合は表示されません) を表します。プロパティ)。</span><span class="sxs-lookup"><span data-stu-id="de274-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="de274-117">このプロパティは、受信時の受信メッセージの自動処理を支援します。</span><span class="sxs-lookup"><span data-stu-id="de274-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="de274-118">トランスポートプロバイダーのオプションでは、このプロパティに FALSE が含まれているか、またはメッセージングユーザーが受信者テーブルに直接記載されていない場合は含まれません。</span><span class="sxs-lookup"><span data-stu-id="de274-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="de274-119">配布リストを展開した結果としてメッセージを配信しても、このプロパティは設定されません。</span><span class="sxs-lookup"><span data-stu-id="de274-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="de274-120">受信者は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de274-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="de274-121">通常、未送信メッセージは、このプロパティ、 **PR_MESSAGE_CC_ME**、または**PR_MESSAGE_TO_ME**を設定しません。</span><span class="sxs-lookup"><span data-stu-id="de274-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="de274-122">ユーザーがパブリックメッセージストア、その他のユーザーのプライベートストア、ディスク上のファイル、またはその他の受信メッセージ内に埋め込まれているメッセージ内に存在する場合は、通常、トランスポートプロバイダーの最終時刻に設定された値が含まれています。メッセージを配信した。</span><span class="sxs-lookup"><span data-stu-id="de274-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="de274-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="de274-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de274-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="de274-124">Protocol specifications</span></span>

<span data-ttu-id="de274-125">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de274-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de274-126">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="de274-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de274-127">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de274-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de274-128">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="de274-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de274-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="de274-129">Header files</span></span>

<span data-ttu-id="de274-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de274-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="de274-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="de274-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="de274-132">Mapitags</span><span class="sxs-lookup"><span data-stu-id="de274-132">Mapitags.h</span></span>
  
> <span data-ttu-id="de274-133">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de274-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de274-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="de274-134">See also</span></span>



[<span data-ttu-id="de274-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="de274-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de274-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de274-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de274-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de274-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de274-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de274-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

