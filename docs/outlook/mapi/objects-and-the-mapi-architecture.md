---
title: オブジェクトと MAPI アーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279790"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="24dd4-103">オブジェクトと MAPI アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="24dd4-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="24dd4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24dd4-105">MAPI で定義されるオブジェクトはすべて、MAPI アーキテクチャの 1 つ以上のレイヤーに含まれます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="24dd4-106">クライアント インターフェイス層には、クライアント アプリケーション、フォーム ビューアー、またはフォーム サーバーが実装できるすべてのオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24dd4-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="24dd4-107">サービス プロバイダー インターフェイス層には、任意の種類のサービス プロバイダーが実装できるオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24dd4-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="24dd4-108">このレイヤーには、アドレス帳、メッセージ ストア、トランスポート プロバイダー、フォーム ライブラリによって実装されたオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="24dd4-109">MAPI サブシステムを表すレイヤーは、クライアント インターフェイス層とサービス プロバイダー インターフェイス層の間に配置されます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="24dd4-110">MAPI レイヤーには、MAPI がクライアントまたはサービス プロバイダーが使用するために実装するオブジェクトすべてが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24dd4-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="24dd4-111">次の図は、各 MAPI オブジェクトが MAPI アーキテクチャに適合する場所を示しています。</span><span class="sxs-lookup"><span data-stu-id="24dd4-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="24dd4-112">オブジェクトは、派生インターフェイスの名前で表されます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="24dd4-113">たとえば、アドバイス シンク オブジェクトは [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) [、IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) から派生するインターフェイス、およびすべてのアアドバイス シンク オブジェクトが実装するインターフェイスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="24dd4-114">ブリッジ 層を構成するインターフェイスは、複数のコンポーネントで使用または実装されます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="24dd4-115">MAPI レイヤーは、クライアント層とプロバイダー層を分離する場合に表示されます。つまり、すべての通信が MAPI を経由する必要があります。これは当てはめではありません。</span><span class="sxs-lookup"><span data-stu-id="24dd4-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="24dd4-116">クライアントは、サービス プロバイダー オブジェクトと直接通信できます。</span><span class="sxs-lookup"><span data-stu-id="24dd4-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="24dd4-117">**MAPI のオブジェクト レイヤー**</span><span class="sxs-lookup"><span data-stu-id="24dd4-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="24dd4-118">MAPI![の MAPI オブジェクト](media/amapi_38.gif "レイヤー内のオブジェクトレイヤー")</span><span class="sxs-lookup"><span data-stu-id="24dd4-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24dd4-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="24dd4-119">See also</span></span>

- [<span data-ttu-id="24dd4-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24dd4-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="24dd4-121">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="24dd4-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

