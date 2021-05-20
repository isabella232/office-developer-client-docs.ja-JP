---
title: MAPI トランスポート プロバイダー オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430358"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="74c6f-103">MAPI トランスポート プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74c6f-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="74c6f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74c6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74c6f-105">すべてのサービス プロバイダーによって実装される標準のプロバイダー オブジェクトとログオン オブジェクトに加えて、状態オブジェクトを実装するためにトランスポート プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="74c6f-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="74c6f-106">その他のサービス プロバイダーの種類では、status オブジェクトの実装はオプションです。</span><span class="sxs-lookup"><span data-stu-id="74c6f-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="74c6f-107">ただし、MAPI はトランスポート プロバイダーに対して必要です。</span><span class="sxs-lookup"><span data-stu-id="74c6f-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="74c6f-108">リモート サーバーからのメッセージ ヘッダーのダウンロードをサポートするトランスポート プロバイダーは、フォルダーとテーブルも実装します。</span><span class="sxs-lookup"><span data-stu-id="74c6f-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="74c6f-109">次の図は、トランスポート プロバイダーが対応するインターフェイスで実装できる各オブジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="74c6f-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="74c6f-110">図は、MAPI またはクライアントがオブジェクトのユーザーかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="74c6f-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="74c6f-111">![トランスポート プロバイダーが実装するオブジェクト](media/amapi_66.gif "トランスポート プロバイダーが実装するオブジェクト")</span><span class="sxs-lookup"><span data-stu-id="74c6f-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74c6f-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="74c6f-112">See also</span></span>

- [<span data-ttu-id="74c6f-113">MAPI サービス プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="74c6f-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

