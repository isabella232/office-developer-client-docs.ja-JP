---
title: PidTagMessageCcMe の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8e1578da3a9caea7533b75fe6dc16c3d7c3488d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802965"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="3a299-103">PidTagMessageCcMe の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3a299-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="3a299-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a299-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a299-105">このメッセージングのユーザーを選択し、具体的にはこのメッセージのカーボン コピー (CC) 受信者という配布リストの一部ではない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="3a299-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a299-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3a299-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a299-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="3a299-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="3a299-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3a299-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a299-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="3a299-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="3a299-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3a299-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a299-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3a299-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3a299-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3a299-112">Area:</span></span>  <br/> |<span data-ttu-id="3a299-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="3a299-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a299-114">備考</span><span class="sxs-lookup"><span data-stu-id="3a299-114">Remarks</span></span>

<span data-ttu-id="3a299-115">このプロパティを確認するかどうかユーザー名に明示的にカーボン コピー受信者一覧で、リスト内のすべてのエントリを検査せずに便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="3a299-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="3a299-116">このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。</span><span class="sxs-lookup"><span data-stu-id="3a299-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="3a299-117">トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="3a299-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="3a299-118">配布リストの展開またはブラインド カーボン コピーの指定によるメッセージの配信は、このプロパティを設定するには発生しません。</span><span class="sxs-lookup"><span data-stu-id="3a299-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="3a299-119">受信者は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a299-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="3a299-120">一般に、未送信のメッセージには**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) または**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) は、このプロパティ設定しません。</span><span class="sxs-lookup"><span data-stu-id="3a299-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="3a299-121">ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="3a299-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3a299-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3a299-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a299-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3a299-123">Protocol specifications</span></span>

<span data-ttu-id="3a299-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a299-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a299-125">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3a299-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3a299-126">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a299-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a299-127">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3a299-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a299-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3a299-128">Header files</span></span>

<span data-ttu-id="3a299-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a299-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a299-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3a299-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a299-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3a299-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3a299-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3a299-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a299-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a299-133">See also</span></span>



[<span data-ttu-id="3a299-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3a299-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a299-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3a299-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a299-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3a299-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a299-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3a299-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

