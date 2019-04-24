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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329737"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="c359c-103">PidTagMessageCcMe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c359c-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="c359c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c359c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c359c-105">このメッセージングユーザーが、このメッセージの bcc 受信者として明示的に指定されていて、配布リストの一部ではない場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c359c-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c359c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c359c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c359c-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="c359c-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="c359c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c359c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c359c-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="c359c-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="c359c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c359c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c359c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c359c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c359c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c359c-112">Area:</span></span>  <br/> |<span data-ttu-id="c359c-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c359c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c359c-114">解説</span><span class="sxs-lookup"><span data-stu-id="c359c-114">Remarks</span></span>

<span data-ttu-id="c359c-115">このプロパティを使用すると、リスト内のすべてのエントリを調べることなく、ユーザー名がカーボンコピー受信者一覧に明示的に表示されるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="c359c-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="c359c-116">このプロパティは、受信時の受信メッセージの自動処理にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c359c-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="c359c-117">トランスポートプロバイダーのオプションでは、このプロパティに FALSE が含まれているか、またはメッセージングユーザーが受信者テーブルに直接記載されていない場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="c359c-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="c359c-118">配布リストの展開またはブラインドカーボンコピーの指定によるメッセージ配信が、このプロパティを設定しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c359c-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="c359c-119">受信者は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c359c-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="c359c-120">通常、未送信メッセージは、このプロパティ、 **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))、または**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) を設定しません。</span><span class="sxs-lookup"><span data-stu-id="c359c-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="c359c-121">ユーザーがパブリックメッセージストア、その他のユーザーのプライベートストア、ディスク上のファイル、またはその他の受信メッセージ内に埋め込まれているメッセージ内に存在する場合は、通常、トランスポートプロバイダーの最終時刻に設定された値が含まれています。メッセージを配信した。</span><span class="sxs-lookup"><span data-stu-id="c359c-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c359c-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c359c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c359c-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c359c-123">Protocol specifications</span></span>

<span data-ttu-id="c359c-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c359c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c359c-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c359c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c359c-126">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c359c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c359c-127">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c359c-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c359c-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c359c-128">Header files</span></span>

<span data-ttu-id="c359c-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c359c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c359c-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c359c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c359c-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c359c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c359c-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c359c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c359c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c359c-133">See also</span></span>



[<span data-ttu-id="c359c-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c359c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c359c-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c359c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c359c-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c359c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c359c-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c359c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

