---
title: トランスポートプロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328687"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="d4679-103">トランスポートプロバイダーに必要な機能</span><span class="sxs-lookup"><span data-stu-id="d4679-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="d4679-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4679-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4679-105">すべての MAPI トランスポートプロバイダーは次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4679-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="d4679-106">MAPI およびその他のサービスプロバイダーを使用する場合の一般的なガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="d4679-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="d4679-107">詳細については、「 [mapi アプリケーション開発](mapi-application-development.md)および[mapi サービスプロバイダ](mapi-service-providers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4679-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="d4679-108">トランスポートプロバイダ DLL が MAPI に公開される[](xpproviderinit.md)ようにします。</span><span class="sxs-lookup"><span data-stu-id="d4679-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="d4679-109">[ixpprovider: iunknown](ixpprovideriunknown.md)インターフェイスと[IXPLogon: iunknown](ixplogoniunknown.md)インターフェイスの実装を MAPI に公開します。</span><span class="sxs-lookup"><span data-stu-id="d4679-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="d4679-110">MAPI およびクライアントアプリケーションに対して、 [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスの実装を公開します。</span><span class="sxs-lookup"><span data-stu-id="d4679-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d4679-111">**imapistatus**の実装の詳細については、「 [status オブジェクトの実装](status-object-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4679-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="d4679-112">構成用のプロパティシートダイアログボックスを実装します。</span><span class="sxs-lookup"><span data-stu-id="d4679-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="d4679-113">プロパティシートの実装の詳細については、「[プロパティシートの実装](property-sheet-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4679-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

