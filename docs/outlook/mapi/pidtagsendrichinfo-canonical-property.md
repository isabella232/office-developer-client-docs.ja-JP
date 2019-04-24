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
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342519"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="b1488-103">PidTagSendRichInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1488-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="b1488-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1488-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1488-105">受信者がリッチテキスト形式 (RTF) およびオブジェクトのリンクと埋め込み (OLE) オブジェクトを含む、すべてのメッセージのコンテンツを受信できる場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b1488-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1488-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1488-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1488-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="b1488-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="b1488-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b1488-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1488-109">0x3a40</span><span class="sxs-lookup"><span data-stu-id="b1488-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="b1488-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1488-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1488-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b1488-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b1488-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b1488-112">Area:</span></span>  <br/> |<span data-ttu-id="b1488-113">Address</span><span class="sxs-lookup"><span data-stu-id="b1488-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1488-114">解説</span><span class="sxs-lookup"><span data-stu-id="b1488-114">Remarks</span></span>

<span data-ttu-id="b1488-115">配布リストとメッセージングユーザーオブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b1488-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="b1488-116">このプロパティは、送信者が受信者の MAPI が有効であると判断するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b1488-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="b1488-117">このプロパティが TRUE に設定されている場合、トランスポートとゲートウェイは RTF および OLE オブジェクトを含む、メッセージの完全なコンテンツを送信できます。</span><span class="sxs-lookup"><span data-stu-id="b1488-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="b1488-118">トランスポートプロバイダーとゲートウェイは、トランスポートニュートラルカプセル化形式 (TNEF) を使用して、関連するすべてのメッセージングシステムにネイティブではないすべてのプロパティをカプセル化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1488-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="b1488-119">このプロパティが FALSE に設定されている場合、トランスポートプロバイダーとゲートウェイは、ネイティブクライアントが使用できないメッセージの内容を自由に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="b1488-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="b1488-120">たとえば、クライアントが RTF をサポートしていない場合、トランスポートプロバイダーはプレーンテキストのみを送信できます。</span><span class="sxs-lookup"><span data-stu-id="b1488-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="b1488-121">このプロパティが設定されていない場合、既定の動作は、トランスポートプロバイダー、メッセージ転送エージェント (MTA)、またはゲートウェイの実装によって決まります。</span><span class="sxs-lookup"><span data-stu-id="b1488-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="b1488-122">アドレス帳プロバイダーは、このプロパティをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b1488-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="b1488-123">たとえば、密結合のアドレス帳とトランスポートプロバイダーは、TNEF を送信することはできますが、RTF は使用しません。</span><span class="sxs-lookup"><span data-stu-id="b1488-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="b1488-124">クライアントは、トランスポートプロバイダーとゲートウェイが独自のイニシアチブで TNEF を使用することを想定してはなりません。</span><span class="sxs-lookup"><span data-stu-id="b1488-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="b1488-125">tnef をサポートする一部のトランスポートプロバイダーおよびゲートウェイは、このプロパティの値を考慮せずにメッセージを送信しますが、TRUE に設定されていない場合は、tnef の作成や送信を拒否します。</span><span class="sxs-lookup"><span data-stu-id="b1488-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b1488-126">このプロパティの設定とその値に基づいた決定は、受信者ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="b1488-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="b1488-127">既定では、MAPI は値を TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="b1488-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="b1488-128">[IAddrBook:: createoneoff](iaddrbook-createoneoff.md)または[imapisupport:: createoneoff](imapisupport-createoneoff.md)を呼び出しているクライアントは、 _ulflags_パラメーターで**MAPI_SEND_NO_RICH_INFO**ビットを設定することができます。これにより、MAPI でこのプロパティが FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1488-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="b1488-129">ユーザーインターフェイスによって作成された1回目の一時は、作成するテンプレートで指定された値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1488-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="b1488-130">[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドへの呼び出しでは、名前を解決できないにもかかわらず、インターネットアドレス (SMTP) として解釈される場合、このプロパティは FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1488-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="b1488-131">インターネットアドレスとして解釈されるようにするには、未解決のエントリの表示名を X @ Y の形式にする必要があります。Z ("pete@pinecone.com" など)。</span><span class="sxs-lookup"><span data-stu-id="b1488-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1488-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1488-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1488-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1488-133">Protocol specifications</span></span>

<span data-ttu-id="b1488-134">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1488-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1488-135">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1488-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1488-136">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1488-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1488-137">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1488-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="b1488-138">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1488-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1488-139">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1488-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b1488-140">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1488-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1488-141">インターネット標準の電子メールの規則からメッセージオブジェクトへ。</span><span class="sxs-lookup"><span data-stu-id="b1488-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1488-142">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b1488-142">Header files</span></span>

<span data-ttu-id="b1488-143">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1488-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1488-144">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1488-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1488-145">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b1488-145">Mapitags.h</span></span>
  
> <span data-ttu-id="b1488-146">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b1488-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1488-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1488-147">See also</span></span>



[<span data-ttu-id="b1488-148">PidTagAttachDataObject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1488-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="b1488-149">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b1488-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1488-150">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1488-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1488-151">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1488-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1488-152">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1488-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

