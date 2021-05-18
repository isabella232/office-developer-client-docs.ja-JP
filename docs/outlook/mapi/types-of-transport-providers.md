---
title: トランスポート プロバイダーの種類
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
# <a name="types-of-transport-providers"></a><span data-ttu-id="ed340-103">トランスポート プロバイダーの種類</span><span class="sxs-lookup"><span data-stu-id="ed340-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="ed340-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed340-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed340-105">すべてのトランスポート プロバイダーは、次のようなさまざまな標準機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed340-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="ed340-106">基になるメッセージング システムに適切なセキュリティを提供する。</span><span class="sxs-lookup"><span data-stu-id="ed340-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="ed340-107">基になるメッセージング システムからのメッセージの送受信。</span><span class="sxs-lookup"><span data-stu-id="ed340-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="ed340-108">MAPI スプーラーとクライアント アプリケーションが適切に使用できるよう、トランスポート プロバイダーがサポートするアドレスの種類を公開します。</span><span class="sxs-lookup"><span data-stu-id="ed340-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="ed340-109">特定の受信者の配信を受け入れる。</span><span class="sxs-lookup"><span data-stu-id="ed340-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="ed340-110">さらに、MAPI では、特定のメッセージング システムに特化した 2 種類のプロバイダーがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ed340-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="ed340-111">**トランスポートの種類**</span><span class="sxs-lookup"><span data-stu-id="ed340-111">**Transport type**</span></span>|<span data-ttu-id="ed340-112">**追加された機能**</span><span class="sxs-lookup"><span data-stu-id="ed340-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed340-113">リモート トランスポート</span><span class="sxs-lookup"><span data-stu-id="ed340-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="ed340-114">リモート接続されたクライアントとの相互運用性を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ed340-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="ed340-115">TNEF トランスポート</span><span class="sxs-lookup"><span data-stu-id="ed340-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="ed340-116">MAPI プロパティをサポートしていないメッセージング システムで保持できます。</span><span class="sxs-lookup"><span data-stu-id="ed340-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="ed340-117">TNEF トランスポートは、MAPI プロパティの異なるセットをサポートするメッセージング システム間でメッセージを変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed340-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="ed340-118">TNEF トランスポートでは、MAPI [ITnef : IUnknown](itnefiunknown.md) インターフェイスを使用して、宛先システムが直接表現できないプロパティを、メッセージに添付できるバイナリ データ ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="ed340-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="ed340-119">後で、別の TNEF トランスポートで **ITnef** を使用してデータ ストリームをデコードし、元の MAPI プロパティをクライアント アプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed340-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="ed340-120">さらに、トランスポートでカスタム メッセージ クラスをサポートする必要がある場合は、TNEF のサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="ed340-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="ed340-121">TNEF トランスポートの実装の詳細については、「セキュリティ トランスポート プロバイダー [の開発TNEF-Enabledを参照してください](developing-a-tnef-enabled-transport-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ed340-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="ed340-122">トランスポート プロバイダーがこれらの種類の 1 つではない場合は、ターゲット プラットフォームで使用できる基本的な MAPI 関数とネットワーク機能を使用してトランスポート プロバイダーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed340-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

