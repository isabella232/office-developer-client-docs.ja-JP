---
title: MAPI トランスポートプロバイダーのオブジェクト
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
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="377a3-103">MAPI トランスポートプロバイダーのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="377a3-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="377a3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="377a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="377a3-105">すべてのサービスプロバイダーで実装されている標準のプロバイダーおよびログオンオブジェクトに加えて、status オブジェクトを実装するには、トランスポートプロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="377a3-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="377a3-106">その他のサービスプロバイダーの種類については、status オブジェクトを実装することはオプションです。</span><span class="sxs-lookup"><span data-stu-id="377a3-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="377a3-107">ただし、MAPI はトランスポートプロバイダーに対して必須です。</span><span class="sxs-lookup"><span data-stu-id="377a3-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="377a3-108">リモートサーバーからのメッセージヘッダーのダウンロードをサポートするトランスポートプロバイダーも、フォルダーとテーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="377a3-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="377a3-109">次の図は、トランスポートプロバイダーが対応するインターフェイスと共に実装できる各オブジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="377a3-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="377a3-110">この図は、MAPI またはクライアントがオブジェクトのユーザーであるかどうかも示しています。</span><span class="sxs-lookup"><span data-stu-id="377a3-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="377a3-111">![トランスポートプロバイダーが実装するオブジェクト](media/amapi_66.gif "トランスポートプロバイダーが実装するオブジェクト")</span><span class="sxs-lookup"><span data-stu-id="377a3-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="377a3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="377a3-112">See also</span></span>

- [<span data-ttu-id="377a3-113">MAPI サービスプロバイダオブジェクト</span><span class="sxs-lookup"><span data-stu-id="377a3-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

