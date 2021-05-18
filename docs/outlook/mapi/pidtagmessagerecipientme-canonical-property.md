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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325621"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="00588-103">PidTagMessageRecipientMe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00588-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="00588-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00588-105">このメッセージング ユーザーが、このメッセージのプライマリ (To)、カーボン コピー (CC)、またはブラインド カーボン コピー (BCC) 受信者として特別に名前が付け、配布リストの一部ではない場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="00588-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00588-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="00588-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00588-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="00588-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="00588-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="00588-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00588-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="00588-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="00588-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="00588-110">Data type:</span></span>  <br/> |<span data-ttu-id="00588-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="00588-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="00588-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="00588-112">Area:</span></span>  <br/> |<span data-ttu-id="00588-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="00588-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00588-114">注釈</span><span class="sxs-lookup"><span data-stu-id="00588-114">Remarks</span></span>

<span data-ttu-id="00588-115">このプロパティは、リスト内のすべてのエントリを調べることなく、ユーザー名が受信者リストに明示的に表示されるかどうかを判断する便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="00588-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="00588-116">この値は、プロパティ **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) と **PR_MESSAGE_TO_ME** ([PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)の論理 **OR** 操作と、BCC 情報 (プロパティに表示されない) を表します。</span><span class="sxs-lookup"><span data-stu-id="00588-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="00588-117">このプロパティは、受信時に受信したメッセージの自動処理を支援します。</span><span class="sxs-lookup"><span data-stu-id="00588-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="00588-118">トランスポート プロバイダーのオプションでは、このプロパティに FALSE が含まれているか、メッセージング ユーザーが受信者テーブルに直接表示されていない場合は含まれません。</span><span class="sxs-lookup"><span data-stu-id="00588-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="00588-119">配布リストの展開によるメッセージ配信では、このプロパティは設定されません。</span><span class="sxs-lookup"><span data-stu-id="00588-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="00588-120">受信者の名前は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00588-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="00588-121">一般に、メッセージの送信を解除すると、このプロパティ、PR_MESSAGE_CC_ME、PR_MESSAGE_TO_ME は **設定されません**。</span><span class="sxs-lookup"><span data-stu-id="00588-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="00588-122">ユーザーがメッセージに存在する場合、ユーザーはパブリック メッセージ ストア、他のユーザーのプライベート ストア、ディスク上のファイル、または他の受信メッセージ内に埋め込まれている場合、通常、トランスポート プロバイダーがメッセージを最後に配信した時刻に設定された値を含みます。</span><span class="sxs-lookup"><span data-stu-id="00588-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00588-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="00588-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00588-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="00588-124">Protocol specifications</span></span>

<span data-ttu-id="00588-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00588-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00588-126">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="00588-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00588-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00588-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00588-128">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="00588-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00588-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="00588-129">Header files</span></span>

<span data-ttu-id="00588-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00588-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="00588-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="00588-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="00588-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00588-132">Mapitags.h</span></span>
  
> <span data-ttu-id="00588-133">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="00588-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00588-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="00588-134">See also</span></span>



[<span data-ttu-id="00588-135">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="00588-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00588-136">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00588-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00588-137">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="00588-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00588-138">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="00588-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

