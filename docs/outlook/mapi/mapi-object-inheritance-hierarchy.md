---
title: MAPI オブジェクトの継承階層
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345842"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="da9b9-103">MAPI オブジェクトの継承階層</span><span class="sxs-lookup"><span data-stu-id="da9b9-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="da9b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da9b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da9b9-105">MAPI オブジェクトによって実装されたインターフェイスはすべて、最終的に [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)(オブジェクトの通信を可能にする OLE インターフェイス) から継承されます。</span><span class="sxs-lookup"><span data-stu-id="da9b9-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="da9b9-106">ほとんどのインターフェイスは **IUnknown** から直接継承しますが [、IMAPIProp : IUnknown](imapipropiunknown.md) または [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="da9b9-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="da9b9-107">次の図は、MAPI の完全な継承階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="da9b9-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="da9b9-108">**MAPI 継承階層**</span><span class="sxs-lookup"><span data-stu-id="da9b9-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="da9b9-109">![MAPI 継承階層](media/amapi_06.gif "MAPI 継承階層")</span><span class="sxs-lookup"><span data-stu-id="da9b9-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da9b9-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="da9b9-110">See also</span></span>

- [<span data-ttu-id="da9b9-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da9b9-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="da9b9-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="da9b9-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="da9b9-113">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="da9b9-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

