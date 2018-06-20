---
title: MAPI オブジェクトの継承階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801398"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="f5649-103">MAPI オブジェクトの継承階層</span><span class="sxs-lookup"><span data-stu-id="f5649-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="f5649-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5649-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5649-105">MAPI オブジェクトによって実装されるすべてのインタ フェースは、最終的には、 [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)を通信するためにオブジェクトを有効にする OLE インターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="f5649-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="f5649-106">ほとんどのインターフェイスは、 **IUnknown**から直接継承するが、他の 2 つの基本インターフェイスのいずれかの一部を継承: [IMAPIProp: IUnknown](imapipropiunknown.md)または[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="f5649-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="f5649-107">次の図では、MAPI の完全な継承階層を示します。</span><span class="sxs-lookup"><span data-stu-id="f5649-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="f5649-108">**MAPI の継承の階層構造**</span><span class="sxs-lookup"><span data-stu-id="f5649-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="f5649-109">![MAPI の継承の階層構造](media/amapi_06.gif "MAPI の継承の階層構造")</span><span class="sxs-lookup"><span data-stu-id="f5649-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5649-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5649-110">See also</span></span>

- [<span data-ttu-id="f5649-111">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5649-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="f5649-112">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f5649-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="f5649-113">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="f5649-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

