---
title: メッセージ ストア プロバイダーの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426423"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="b9f1f-103">メッセージ ストア プロバイダーの構造</span><span class="sxs-lookup"><span data-stu-id="b9f1f-103">Structure of message store providers</span></span>
  
<span data-ttu-id="b9f1f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9f1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9f1f-105">メッセージ ストア プロバイダーは、メモリ内で実行されている場合は [、IMSProvider : IUnknown インターフェイス](imsprovideriunknown.md) です。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="b9f1f-106">**IMSProvider インターフェイスを使用** すると、クライアント アプリケーションと MAPI スプーラーは、メッセージ ストアへのログオンとオフを行えます。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="b9f1f-107">クライアント アプリケーションと MAPI スプーラーがメッセージ ストア内のフォルダーとメッセージにアクセスするために使用するインターフェイスは [、IMSLogon](imslogoniunknown.md) インターフェイスと [IMsgStore](imsgstoreimapiprop.md) インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="b9f1f-108">これらのインターフェイスは、通常、メッセージ ストアが最初にログオンするときに作成されます。ただし、メッセージ ストア DLL の [MSProviderInit](msproviderinit.md) エントリ ポイントも作成できます。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="b9f1f-109">**IMSLogon** インターフェイスと **IMsgStore** インターフェイスは一部のメソッドを共有しますので、これらの両方のインターフェイスから継承するクラス オブジェクトを 1 つ作成する方が簡単な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="b9f1f-110">これらのインターフェイスを個別のオブジェクトに実装し **、IMSLogon** インターフェイスと **IMsgStore** インターフェイスのメソッドから呼び出す共有メソッドを実装するヘルパー関数を DLL に記述することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="b9f1f-111">次の図は、実行中のメッセージ ストア内のオブジェクト階層の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="b9f1f-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="b9f1f-112">**メッセージ ストアのオブジェクト階層**</span><span class="sxs-lookup"><span data-stu-id="b9f1f-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="b9f1f-113">![メッセージ ストア オブジェクト階層](media/storeobj.gif "メッセージ ストア オブジェクト階層")</span><span class="sxs-lookup"><span data-stu-id="b9f1f-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9f1f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9f1f-114">See also</span></span>

- [<span data-ttu-id="b9f1f-115">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="b9f1f-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

