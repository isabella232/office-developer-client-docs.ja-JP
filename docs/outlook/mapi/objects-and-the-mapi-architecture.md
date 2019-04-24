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
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="15a15-103">オブジェクトと MAPI アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="15a15-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="15a15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15a15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15a15-105">mapi で定義されているすべてのオブジェクトは、mapi アーキテクチャの1つ以上のレイヤーに分類されます。</span><span class="sxs-lookup"><span data-stu-id="15a15-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="15a15-106">クライアントインターフェイスレイヤーには、クライアントアプリケーション、フォームビューアー、またはフォームサーバーが実装できるすべてのオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a15-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="15a15-107">サービスプロバイダインターフェイスレイヤーには、任意の種類のサービスプロバイダーが実装できるオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a15-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="15a15-108">このレイヤーには、アドレス帳、メッセージストア、トランスポートプロバイダー、およびフォームライブラリによって実装されるオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="15a15-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="15a15-109">MAPI サブシステムを表すレイヤーは、クライアントとサービスプロバイダのインターフェイス層の間に配置されます。</span><span class="sxs-lookup"><span data-stu-id="15a15-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="15a15-110">mapi 層には、クライアントまたはサービスプロバイダーが使用するために mapi が実装するすべてのオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="15a15-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="15a15-111">次の図は、mapi の各オブジェクトが mapi アーキテクチャに適合する場所を示しています。</span><span class="sxs-lookup"><span data-stu-id="15a15-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="15a15-112">オブジェクトは、派生したインターフェイスの名前で表されます。</span><span class="sxs-lookup"><span data-stu-id="15a15-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="15a15-113">たとえば、アドバイズシンクオブジェクトは[IMAPIAdviseSink: iunknown](imapiadvisesinkiunknown.md)として表示されます。このインターフェイスは、すべてのアドバイズシンクオブジェクトに実装されているので[iunknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から派生しています。</span><span class="sxs-lookup"><span data-stu-id="15a15-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="15a15-114">レイヤーをブリッジするインターフェイスは、複数のコンポーネントによって使用されているか、実装されています。</span><span class="sxs-lookup"><span data-stu-id="15a15-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="15a15-115">mapi 層は、クライアント層とプロバイダー層を分離して表示されますが、すべての通信は MAPI を経由する必要があるということを意味しますが、そうではありません。</span><span class="sxs-lookup"><span data-stu-id="15a15-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="15a15-116">クライアントは、サービスプロバイダオブジェクトに直接通信できます。</span><span class="sxs-lookup"><span data-stu-id="15a15-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="15a15-117">**MAPI のオブジェクト レイヤー**</span><span class="sxs-lookup"><span data-stu-id="15a15-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="15a15-118">![MAPI のオブジェクトレイヤー](media/amapi_38.gif "MAPI のオブジェクトレイヤー")</span><span class="sxs-lookup"><span data-stu-id="15a15-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15a15-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="15a15-119">See also</span></span>

- [<span data-ttu-id="15a15-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15a15-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="15a15-121">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="15a15-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

