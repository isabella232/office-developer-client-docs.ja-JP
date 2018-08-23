---
title: オブジェクト、および MAPI アーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e89c2ad37b700a977962e5e0ff0ca30b9d910e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801688"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="4b5cc-103">オブジェクト、および MAPI アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="4b5cc-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="4b5cc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b5cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b5cc-105">すべての MAPI を定義するオブジェクトは、MAPI アーキテクチャでは、1 つまたは複数のレイヤーに分けられます。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="4b5cc-106">クライアント ・ インタ フェース ・ レイヤーには、クライアント アプリケーション、フォームのビューアー、またはフォームのサーバーを実装するすべてのオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="4b5cc-107">サービス プロバイダー インターフェイス層には、任意の型のサービス ・ プロバイダーを実装するオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="4b5cc-108">このレイヤーには、アドレス帳、メッセージ ・ ストア、トランスポート プロバイダー、およびフォーム ライブラリで実装されているオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="4b5cc-109">MAPI のサブシステムを表すレイヤーは、クライアントとサービス プロバイダーのインターフェイス層の間に配置されます。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="4b5cc-110">MAPI のレイヤーには、すべての MAPI を使用するには、クライアントまたはサービス プロバイダーの実装するオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="4b5cc-111">MAPI オブジェクトの組み込まれているか、MAPI アーキテクチャを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="4b5cc-112">オブジェクトは、派生インターフェイスの名前で表されます。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="4b5cc-113">アドバイズ シンク オブジェクトを表示するたとえば、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)、 [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から派生して、すべてのアドバイズ シンク オブジェクトを実装するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="4b5cc-114">レイヤーを埋めるためのインタ フェースは、使用か、または複数のコンポーネントによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="4b5cc-115">すべての通信が、MAPI を介してフローする必要があることを暗に示して、クライアントとプロバイダー層を分離するのには MAPI のレイヤーが表示されますが、そうではないです。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="4b5cc-116">クライアントことができ、サービス ・ プロバイダーのオブジェクトと直接通信を行います。</span><span class="sxs-lookup"><span data-stu-id="4b5cc-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="4b5cc-117">**MAPI のオブジェクト レイヤー**</span><span class="sxs-lookup"><span data-stu-id="4b5cc-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="4b5cc-118">![MAPI オブジェクト レイヤー](media/amapi_38.gif "MAPI オブジェクト レイヤー")</span><span class="sxs-lookup"><span data-stu-id="4b5cc-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b5cc-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b5cc-119">See also</span></span>

- [<span data-ttu-id="4b5cc-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b5cc-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="4b5cc-121">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="4b5cc-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

