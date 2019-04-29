---
title: トランスポートプロバイダーの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406165"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="26dea-103">トランスポートプロバイダーの種類</span><span class="sxs-lookup"><span data-stu-id="26dea-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="26dea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26dea-105">すべてのトランスポートプロバイダーは、次のような幅広い標準的な機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="26dea-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="26dea-106">基になるメッセージングシステムに適切なセキュリティを提供する。</span><span class="sxs-lookup"><span data-stu-id="26dea-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="26dea-107">基になるメッセージングシステムからメッセージを送受信する。</span><span class="sxs-lookup"><span data-stu-id="26dea-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="26dea-108">トランスポートプロバイダーがサポートするアドレスの種類を公開することで、MAPI スプーラーおよびクライアントアプリケーションはそれらを適切に使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="26dea-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="26dea-109">特定の受信者に対して配信を承諾します。</span><span class="sxs-lookup"><span data-stu-id="26dea-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="26dea-110">さらに、MAPI は、特定のメッセージングシステムに対して2つの専用のプロバイダーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="26dea-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="26dea-111">**トランスポートの種類**</span><span class="sxs-lookup"><span data-stu-id="26dea-111">**Transport type**</span></span>|<span data-ttu-id="26dea-112">**機能の追加**</span><span class="sxs-lookup"><span data-stu-id="26dea-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26dea-113">リモートトランスポート</span><span class="sxs-lookup"><span data-stu-id="26dea-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="26dea-114">リモート接続されたクライアントとの相互運用性を有効にします。</span><span class="sxs-lookup"><span data-stu-id="26dea-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="26dea-115">TNEF トランスポート</span><span class="sxs-lookup"><span data-stu-id="26dea-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="26dea-116">MAPI プロパティをサポートしていないメッセージングシステムで、MAPI プロパティを保持できるようにします。</span><span class="sxs-lookup"><span data-stu-id="26dea-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="26dea-117">TNEF トランスポートは、MAPI プロパティの異なるセットをサポートするメッセージングシステム間でメッセージを変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26dea-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="26dea-118">[TNEF トランスポート] MAPI [ITnef: IUnknown](itnefiunknown.md)インターフェイスを使用して、宛先システムがメッセージに添付できるバイナリデータストリームに直接表すことができないすべてのプロパティを変換します。</span><span class="sxs-lookup"><span data-stu-id="26dea-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="26dea-119">その後、別の TNEF トランスポートで**ITnef**を使用してデータストリームをデコードし、クライアントアプリケーションで元の MAPI プロパティを使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="26dea-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="26dea-120">また、トランスポートがカスタムメッセージクラスをサポートする必要がある場合は、TNEF のサポートが必要になります。</span><span class="sxs-lookup"><span data-stu-id="26dea-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="26dea-121">tnef トランスポートの実装については、「 [tnef 対応のトランスポートプロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="26dea-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="26dea-122">トランスポートプロバイダーがこれらの種類のいずれにも該当しない場合は、ターゲットプラットフォームで利用できる基本的な MAPI 機能とネットワーク関数を使用して実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26dea-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

