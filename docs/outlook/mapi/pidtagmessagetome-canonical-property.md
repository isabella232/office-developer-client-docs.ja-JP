---
title: PidTagMessageToMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 51a8f1768f9b4ed859989058c66044c807068386
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583933"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="1c0c5-103">PidTagMessageToMe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c0c5-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="1c0c5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c0c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c0c5-105">このメッセージング ユーザーが具体的には (このメッセージの受信者宛先) プライマリという配布リストの一部ではない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c0c5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1c0c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c0c5-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="1c0c5-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="1c0c5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1c0c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c0c5-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="1c0c5-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="1c0c5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1c0c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c0c5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1c0c5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1c0c5-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1c0c5-112">Area:</span></span>  <br/> |<span data-ttu-id="1c0c5-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="1c0c5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c0c5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1c0c5-114">Remarks</span></span>

<span data-ttu-id="1c0c5-115">このプロパティを確認するかどうかユーザー名に明示的に、プライマリ受信者ボックスの一覧で、リスト内のすべてのエントリを検査せずに便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="1c0c5-116">このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="1c0c5-117">トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="1c0c5-118">配布リストの展開またはブラインド カーボン コピーの指定によるメッセージの配信は、このプロパティを設定するには発生しません。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="1c0c5-119">受信者は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="1c0c5-120">未送信メッセージ一般には設定されません ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))、 **PR_MESSAGE_CC_ME** 、 **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))、またはこのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="1c0c5-121">ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c0c5-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1c0c5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c0c5-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1c0c5-123">Protocol specifications</span></span>

<span data-ttu-id="1c0c5-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0c5-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0c5-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c0c5-126">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0c5-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0c5-127">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c0c5-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1c0c5-128">Header files</span></span>

<span data-ttu-id="1c0c5-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c0c5-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c0c5-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c0c5-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c0c5-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1c0c5-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c0c5-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c0c5-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c0c5-133">See also</span></span>



[<span data-ttu-id="1c0c5-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c0c5-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c0c5-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c0c5-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c0c5-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1c0c5-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c0c5-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1c0c5-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

