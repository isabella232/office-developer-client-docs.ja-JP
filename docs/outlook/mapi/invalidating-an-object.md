---
title: オブジェクトの無効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566475"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="7849d-103">オブジェクトの無効化</span><span class="sxs-lookup"><span data-stu-id="7849d-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="7849d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7849d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7849d-105">プロバイダーのシャット ダウン プロセスの一環として、オブジェクトを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7849d-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="7849d-106">オブジェクトが無効では、vtable と vtable が同じ 3 つの**IUnknown**メソッドの実装が含まれている: **AddRef**、**リリース**、および**バージョン管理規則によって**。</span><span class="sxs-lookup"><span data-stu-id="7849d-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="7849d-107">[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)、3 つの一般的なプロバイダーの種類のそれぞれのサポート オブジェクトに含まれるメソッドを呼び出すことによってオブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7849d-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="7849d-108">プロバイダーは、通常、ログオン オブジェクトの**ログオフ時**のメソッドの実装ではこの呼び出しを作成します。</span><span class="sxs-lookup"><span data-stu-id="7849d-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="7849d-109">MAPI オブジェクトに関連付けられているメモリを解放する最終的な責任は、オブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="7849d-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="7849d-110">すべてのオブジェクトに接続されているリソースを解放し、すべての継承されたインターフェイスのメソッドを無効にする**MakeInvalid**を呼び出してできます。</span><span class="sxs-lookup"><span data-stu-id="7849d-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="7849d-111">これらのメソッドへの呼び出しには、MAPI_E_INVALID_OBJECT が返されます。</span><span class="sxs-lookup"><span data-stu-id="7849d-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="7849d-112">**MakeInvalid**を使用して、無視するように多くのサービス プロバイダーを選択するオプションです。</span><span class="sxs-lookup"><span data-stu-id="7849d-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7849d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="7849d-113">See also</span></span>



[<span data-ttu-id="7849d-114">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="7849d-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

