---
title: PidTagSendRichInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a85851663c22b33ea94099ac0ab14f81c424259b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803511"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="6d84f-103">PidTagSendRichInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d84f-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="6d84f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d84f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d84f-105">受信者がリッチ テキスト形式 (RTF) およびオブジェクトのリンクと埋め込み (OLE) オブジェクトを含む、すべてのメッセージの内容を受信できる場合は TRUE を格納します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d84f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6d84f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d84f-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="6d84f-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="6d84f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6d84f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d84f-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="6d84f-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="6d84f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6d84f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d84f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6d84f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6d84f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6d84f-112">Area:</span></span>  <br/> |<span data-ttu-id="6d84f-113">Address</span><span class="sxs-lookup"><span data-stu-id="6d84f-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d84f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6d84f-114">Remarks</span></span>

<span data-ttu-id="6d84f-115">配布リストとメッセージのユーザー オブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6d84f-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="6d84f-116">このプロパティでは、送信者が受信者に MAPI を有効にすると見なされるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="6d84f-117">このプロパティは TRUE に設定、トランスポートおよびゲートウェイは RTF と OLE オブジェクトを含むメッセージの完全なコンテンツを送信できます。</span><span class="sxs-lookup"><span data-stu-id="6d84f-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="6d84f-118">トランスポート プロバイダーが、ゲートウェイは、すべてのメッセージング ・ システムにネイティブではない任意のプロパティをカプセル化するのには、トランスポート ニュートラル カプセル化形式 (TNEF) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d84f-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="6d84f-119">このプロパティは FALSE に設定、トランスポート プロバイダーが、ゲートウェイは、ネイティブのクライアントが使用できないメッセージの内容を破棄するのには無料です。</span><span class="sxs-lookup"><span data-stu-id="6d84f-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="6d84f-120">など、クライアントでは、rtf 形式をサポートしていないと、トランスポート プロバイダーはプレーン テキストのみを送信できます。</span><span class="sxs-lookup"><span data-stu-id="6d84f-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="6d84f-121">このプロパティが設定されていない場合、既定の動作は、トランスポート プロバイダー、メッセージ転送エージェント (MTA) またはゲートウェイの実装によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="6d84f-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="6d84f-122">アドレス帳プロバイダーは、このプロパティをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6d84f-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="6d84f-123">たとえば、密結合のアドレス帳とトランスポート プロバイダーは、TNEF を送信する rtf 形式を使用しない選択できます。</span><span class="sxs-lookup"><span data-stu-id="6d84f-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="6d84f-124">トランスポート プロバイダーを考えないで、クライアントとゲートウェイでは、TNEF を使用して、自分の責任では。</span><span class="sxs-lookup"><span data-stu-id="6d84f-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="6d84f-125">いくつかのトランスポート プロバイダーと TNEF をサポートするゲートウェイは、このプロパティの値に関係なく転送が構築または TRUE に設定されていない場合は、TNEF を送信する他のユーザーを拒否します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6d84f-126">受信者ごとの単位では、このプロパティと、その値に基づく意思決定の設定です。</span><span class="sxs-lookup"><span data-stu-id="6d84f-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="6d84f-127">既定では、MAPI は、値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="6d84f-128">[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)または[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を呼び出して、プロバイダーを呼び出すクライアントは、 _ulFlags_パラメーターを FALSE にこのプロパティを設定するのには MAPI に**MAPI_SEND_NO_RICH_INFO**ビットを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d84f-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="6d84f-129">ユーザー インターフェイスによって作成される一時アドレスは、作成するテンプレートで指定された値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="6d84f-130">[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドの呼び出しの名前が解決することはできませんが、インターネット アドレス (SMTP) として解釈できる場合、このプロパティは FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="6d84f-131">インターネット アドレスとして解釈されます、未解決のエントリの表示名は、X@Y の形式である必要があります。Z では、"pete@pinecone.com"などです。</span><span class="sxs-lookup"><span data-stu-id="6d84f-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d84f-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6d84f-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d84f-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6d84f-133">Protocol specifications</span></span>

<span data-ttu-id="6d84f-134">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d84f-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d84f-135">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d84f-136">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d84f-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d84f-137">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6d84f-138">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d84f-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d84f-139">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6d84f-140">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d84f-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d84f-141">メッセージ オブジェクトをインターネット メールの標準的な規則。</span><span class="sxs-lookup"><span data-stu-id="6d84f-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d84f-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6d84f-142">Header files</span></span>

<span data-ttu-id="6d84f-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d84f-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d84f-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6d84f-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d84f-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d84f-145">Mapitags.h</span></span>
  
> <span data-ttu-id="6d84f-146">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d84f-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d84f-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d84f-147">See also</span></span>



[<span data-ttu-id="6d84f-148">PidTagAttachDataObject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d84f-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="6d84f-149">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d84f-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d84f-150">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6d84f-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d84f-151">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6d84f-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d84f-152">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6d84f-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

