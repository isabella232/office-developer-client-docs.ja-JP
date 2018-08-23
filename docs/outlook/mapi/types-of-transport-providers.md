---
title: トランスポート プロバイダーの種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804144"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="5fb29-103">トランスポート プロバイダーの種類</span><span class="sxs-lookup"><span data-stu-id="5fb29-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="5fb29-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fb29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fb29-105">すべてのトランスポート プロバイダーは、次のように、標準的な機能の範囲をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5fb29-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="5fb29-106">基になるメッセージング システムに適切なセキュリティを提供します。</span><span class="sxs-lookup"><span data-stu-id="5fb29-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="5fb29-107">送信して、基になるメッセージング システムからメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="5fb29-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="5fb29-108">アドレスの種類を公開するトランスポート プロバイダーをサポートして、MAPI スプーラーとクライアント アプリケーションを使用できるように、適切にします。</span><span class="sxs-lookup"><span data-stu-id="5fb29-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="5fb29-109">特定の受信者に対する配信を拒否します。</span><span class="sxs-lookup"><span data-stu-id="5fb29-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="5fb29-110">さらに、MAPI は、メッセージング システムの特定のプロバイダーの 2 つの特殊化された型をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5fb29-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="5fb29-111">**トランスポートの種類**</span><span class="sxs-lookup"><span data-stu-id="5fb29-111">**Transport type**</span></span>|<span data-ttu-id="5fb29-112">**機能を追加**</span><span class="sxs-lookup"><span data-stu-id="5fb29-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fb29-113">リモート トランスポート</span><span class="sxs-lookup"><span data-stu-id="5fb29-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="5fb29-114">リモートで接続されているクライアントとの相互運用性を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5fb29-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="5fb29-115">TNEF の転送</span><span class="sxs-lookup"><span data-stu-id="5fb29-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="5fb29-116">メッセージングをサポートしていないシステム上に保存し、MAPI プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fb29-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="5fb29-117">TNEF の配送は、別の MAPI プロパティのセットをサポートしているメッセージング システム間でメッセージを変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5fb29-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="5fb29-118">TNEF の転送は、MAPI を使用して[ITnef: IUnknown](itnefiunknown.md)メッセージに関連付けることができるバイナリ データ ストリームに直接ターゲット ・ システムを表すことはできません任意のプロパティを変換するためのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="5fb29-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="5fb29-119">以降では、TNEF の別のトランスポートでは、データ ストリームをデコードし、元の MAPI プロパティをクライアント アプリケーションで使用できるように**ITnef**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5fb29-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="5fb29-120">さらに、カスタム メッセージ クラスをサポートするために、トランスポートが必要な場合は、TNEF のサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="5fb29-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="5fb29-121">TNEF の転送を実装する方法の詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5fb29-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="5fb29-122">トランスポート プロバイダーがこれらの種類のいずれかでない場合は、基本の MAPI 関数と、ターゲット ・ プラットフォームで利用可能なネットワークの機能を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fb29-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

