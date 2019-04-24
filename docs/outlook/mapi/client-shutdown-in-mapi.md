---
title: MAPI でのクライアント シャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 04ec21b8-8cd8-4d2d-92e7-aa73f4315e1e
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: f2d41ad36472f39e434e3f17757559ada5e08fbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334854"
---
# <a name="client-shutdown-in-mapi"></a><span data-ttu-id="7f771-103">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="7f771-103">Client Shutdown in MAPI</span></span> 
  
<span data-ttu-id="7f771-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f771-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f771-105">microsoft outlook 2010 以降では、microsoft outlook 2013 を含む MAPI クライアントは、以前と同じ方法でシャットダウンするか、高速シャットダウンを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f771-105">Beginning in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, MAPI clients can shut down the same way as before, or they can use fast shutdown.</span></span> <span data-ttu-id="7f771-106">高速シャットダウンを正常に実行するには、クライアントコンピューターの mapi クライアント、mapi プロバイダー、および管理者が高速シャットダウンをサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f771-106">For fast shutdown to occur successfully, the MAPI client, MAPI provider, and administrator of the client computer have to support fast shutdown.</span></span> 
  
<span data-ttu-id="7f771-107">このセクションのトピックでは、高速シャットダウンを実行するクライアントの MAPI サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7f771-107">The topics in this section describe MAPI support for a client to perform fast shutdown.</span></span>
  
[<span data-ttu-id="7f771-108">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="7f771-108">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
  
> <span data-ttu-id="7f771-109">このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7f771-109">This topic introduces the basic mechanism of fast shutdown.</span></span>
    
[<span data-ttu-id="7f771-110">高速シャットダウンのユーザーオプション</span><span class="sxs-lookup"><span data-stu-id="7f771-110">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)
  
> <span data-ttu-id="7f771-111">このトピックでは、管理者がユーザーの MAPI クライアントに対してユーザーレベルで高速シャットダウンを導入する際に使用できる選択肢について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f771-111">This topic describes the choices available for administrators to adopt fast shutdown at the user level for the user's MAPI clients.</span></span>
    
[<span data-ttu-id="7f771-112">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="7f771-112">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)
  
> <span data-ttu-id="7f771-113">このトピックでは、高速シャットダウンインターフェイスを使用して、MAPI クライアントのシャットダウン時のデータ損失を防止するためのベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7f771-113">This topic recommends best practices to use the fast shutdown interfaces to help prevent data loss during a MAPI client shutdown.</span></span>
    

