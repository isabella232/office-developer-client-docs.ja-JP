---
title: PidTagMessageRecipientMe の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e8ae52df1dd9775f706e2b1b2dc8b17b1f47a0bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803008"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="d4aa4-103">PidTagMessageRecipientMe の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="d4aa4-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="d4aa4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4aa4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4aa4-105">このメッセージング ユーザーが具体的には、プライマリ ()、CC (カーボン コピー)、またはこのメッセージのブラインド カーボン コピー (BCC) 受信者というし、配布リストの一部ではない場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4aa4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4aa4-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="d4aa4-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="d4aa4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d4aa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4aa4-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="d4aa4-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="d4aa4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4aa4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4aa4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4aa4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d4aa4-112">Area:</span></span>  <br/> |<span data-ttu-id="d4aa4-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="d4aa4-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4aa4-114">備考</span><span class="sxs-lookup"><span data-stu-id="d4aa4-114">Remarks</span></span>

<span data-ttu-id="d4aa4-115">このプロパティを確認するかどうかユーザー名に明示的に [受信者の一覧では、リスト内のすべてのエントリを検査せずに便利な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="d4aa4-116">値は**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) と**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) のプロパティと、[bcc] 情報の論理**OR**演算を表します (そうしないと表示されないのはプロパティ)。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="d4aa4-117">このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d4aa4-118">トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d4aa4-119">配布リストの展開から得られるメッセージの配信は、このプロパティを設定するには発生しません。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="d4aa4-120">受信者は明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d4aa4-121">未送信メッセージ一般には設定されませんこのプロパティ、 **PR_MESSAGE_CC_ME**、または**PR_MESSAGE_TO_ME**。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="d4aa4-122">ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4aa4-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d4aa4-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4aa4-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d4aa4-124">Protocol specifications</span></span>

<span data-ttu-id="d4aa4-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4aa4-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4aa4-126">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4aa4-127">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4aa4-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4aa4-128">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4aa4-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d4aa4-129">Header files</span></span>

<span data-ttu-id="d4aa4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4aa4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4aa4-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4aa4-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4aa4-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d4aa4-133">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4aa4-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4aa4-134">See also</span></span>



[<span data-ttu-id="d4aa4-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4aa4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4aa4-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4aa4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4aa4-137">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="d4aa4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4aa4-138">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="d4aa4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

