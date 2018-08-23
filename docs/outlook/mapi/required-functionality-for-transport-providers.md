---
title: トランスポート プロバイダーの必須機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580496"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="a1c98-103">トランスポート プロバイダーの必須機能</span><span class="sxs-lookup"><span data-stu-id="a1c98-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="a1c98-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1c98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1c98-105">すべての MAPI トランスポート プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="a1c98-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="a1c98-106">MAPI およびその他のサービス プロバイダーを操作するための一般的なガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="a1c98-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="a1c98-107">詳細については、 [MAPI アプリケーションの開発](mapi-application-development.md)と[サービスの MAPI プロバイダー](mapi-service-providers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1c98-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="a1c98-108">トランスポート プロバイダーを MAPI DLL の公開、 [XPProviderInit](xpproviderinit.md)の初期化関数があります。</span><span class="sxs-lookup"><span data-stu-id="a1c98-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="a1c98-109">MAPI への実装を公開します[IXPProvider: IUnknown](ixpprovideriunknown.md)と[IXPLogon: IUnknown](ixplogoniunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="a1c98-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="a1c98-110">MAPI およびクライアント アプリケーションへの実装を公開します[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="a1c98-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a1c98-111">**IMAPIStatus**の実装の詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1c98-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="a1c98-112">構成のプロパティ シートのダイアログ ボックスを実装します。</span><span class="sxs-lookup"><span data-stu-id="a1c98-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="a1c98-113">プロパティ シートの実装の詳細については、[プロパティ シートの実装](property-sheet-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1c98-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

