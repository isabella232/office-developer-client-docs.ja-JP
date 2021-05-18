---
title: PidTagMessageCcMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329737"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="9cbdb-103">PidTagMessageCcMe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9cbdb-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="9cbdb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cbdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cbdb-105">このメッセージング ユーザーが、このメッセージのカーボン コピー (CC) 受信者として特別に名前が付け、配布リストの一部ではない場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cbdb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9cbdb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cbdb-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="9cbdb-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="9cbdb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9cbdb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cbdb-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="9cbdb-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="9cbdb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9cbdb-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cbdb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9cbdb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9cbdb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9cbdb-112">Area:</span></span>  <br/> |<span data-ttu-id="9cbdb-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="9cbdb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cbdb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9cbdb-114">Remarks</span></span>

<span data-ttu-id="9cbdb-115">このプロパティは、一覧内のすべてのエントリを調べることなく、ユーザー名がカーボン コピー受信者リストに明示的に表示されるかどうかを判断する便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="9cbdb-116">このプロパティは、受信時の受信メッセージの自動処理も支援します。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="9cbdb-117">トランスポート プロバイダーのオプションでは、このプロパティに FALSE が含まれているか、メッセージング ユーザーが受信者テーブルに直接表示されていない場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="9cbdb-118">配布リストの拡張やブラインド カーボン コピーの指定によって生じるメッセージ配信では、このプロパティは設定されません。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="9cbdb-119">受信者の名前は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="9cbdb-120">一般に、メッセージが送信されていない場合は、このプロパティ 、PR_MESSAGE_RECIP_ME [(PidTagMessageRecipientMe)、](pidtagmessagerecipientme-canonical-property.md)または PR_MESSAGE_TO_ME **(** [PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)**は** 設定されません。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="9cbdb-121">ユーザーがメッセージに存在する場合、ユーザーはパブリック メッセージ ストア、他のユーザーのプライベート ストア、ディスク上のファイル、または他の受信メッセージ内に埋め込まれている場合、通常、トランスポート プロバイダーがメッセージを最後に配信した時刻に設定された値を含みます。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9cbdb-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9cbdb-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cbdb-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9cbdb-123">Protocol specifications</span></span>

<span data-ttu-id="9cbdb-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbdb-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbdb-125">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cbdb-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbdb-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbdb-127">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cbdb-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9cbdb-128">Header files</span></span>

<span data-ttu-id="9cbdb-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cbdb-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cbdb-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cbdb-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cbdb-131">Mapitags.h</span></span>
  
> <span data-ttu-id="9cbdb-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9cbdb-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cbdb-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="9cbdb-133">See also</span></span>



[<span data-ttu-id="9cbdb-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9cbdb-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cbdb-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9cbdb-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cbdb-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9cbdb-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cbdb-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9cbdb-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

