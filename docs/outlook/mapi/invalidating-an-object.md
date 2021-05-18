---
title: オブジェクトの無効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407677"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="8133e-103">オブジェクトの無効化</span><span class="sxs-lookup"><span data-stu-id="8133e-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="8133e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8133e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8133e-105">プロバイダーのシャットダウン プロセスの一環として、オブジェクトを無効にしたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="8133e-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="8133e-106">オブジェクトを無効にするには、その vtable を 3 つの **IUnknown** メソッド (AddRef、Release、QueryInterface) の実装を含む vtable に置き換 **える必要があります**。  </span><span class="sxs-lookup"><span data-stu-id="8133e-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="8133e-107">[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)、3 つの一般的なプロバイダーの種類のそれぞれのサポート オブジェクトに含まれているメソッドを呼び出すことによって、オブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="8133e-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="8133e-108">プロバイダーは通常、ログオン オブジェクトの Logoff メソッドの実装でこの呼 **び出しを行** います。</span><span class="sxs-lookup"><span data-stu-id="8133e-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="8133e-109">オブジェクトを無効にすることで、MAPI はオブジェクトに関連付けられたメモリを解放する最終的な責任を負います。</span><span class="sxs-lookup"><span data-stu-id="8133e-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="8133e-110">オブジェクトに接続されているリソースをすべて解放し **、MakeInvalid** を呼び出して、継承されたインターフェイス内のすべてのメソッドを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="8133e-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="8133e-111">これらのメソッドの呼び出しは、MAPI_E_INVALID_OBJECT。</span><span class="sxs-lookup"><span data-stu-id="8133e-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="8133e-112">**MakeInvalid の使用** は、多くのサービス プロバイダーが無視することを選択するオプションです。</span><span class="sxs-lookup"><span data-stu-id="8133e-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8133e-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="8133e-113">See also</span></span>



[<span data-ttu-id="8133e-114">サービス プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="8133e-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

