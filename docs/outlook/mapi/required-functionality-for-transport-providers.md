---
title: トランスポート プロバイダーに必要な機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404443"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="1afe1-103">トランスポート プロバイダーに必要な機能</span><span class="sxs-lookup"><span data-stu-id="1afe1-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="1afe1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1afe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1afe1-105">すべての MAPI トランスポート プロバイダーは、次の必要があります。</span><span class="sxs-lookup"><span data-stu-id="1afe1-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="1afe1-106">MAPI および他のサービス プロバイダーの操作に関する一般的なガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="1afe1-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="1afe1-107">詳細については [、「MAPI アプリケーション開発と](mapi-application-development.md) [MAPI サービス プロバイダー」を参照してください](mapi-service-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="1afe1-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="1afe1-108">トランスポート プロバイダー DLL を MAPI の [XPProviderInit 初期化関数に](xpproviderinit.md) 公開します。</span><span class="sxs-lookup"><span data-stu-id="1afe1-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="1afe1-109">[IXPProvider : IUnknown](ixpprovideriunknown.md)と[IXPLogon : IUnknown](ixplogoniunknown.md)インターフェイスの実装を MAPI に公開します。</span><span class="sxs-lookup"><span data-stu-id="1afe1-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="1afe1-110">MAPI およびクライアント アプリケーションに対して [IMAPIStatus : IMAPIProp インターフェイスの実装を公開](imapistatusimapiprop.md) します。</span><span class="sxs-lookup"><span data-stu-id="1afe1-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="1afe1-111">**IMAPIStatus** の実装の詳細については、「Status Object Implementation [」を参照してください](status-object-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="1afe1-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="1afe1-112">構成用のプロパティ シート ダイアログ ボックスを実装します。</span><span class="sxs-lookup"><span data-stu-id="1afe1-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="1afe1-113">プロパティ シートの実装の詳細については、「プロパティ シートの [実装」を参照してください](property-sheet-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="1afe1-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

