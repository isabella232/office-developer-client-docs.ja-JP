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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405136"
---
# <a name="client-shutdown-in-mapi"></a><span data-ttu-id="34ab7-103">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="34ab7-103">Client Shutdown in MAPI</span></span> 
  
<span data-ttu-id="34ab7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34ab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34ab7-105">Microsoft Outlook 2013 Microsoft Outlook 2010から、MAPI クライアントは以前と同じ方法でシャットダウンするか、高速シャットダウンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="34ab7-105">Beginning in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, MAPI clients can shut down the same way as before, or they can use fast shutdown.</span></span> <span data-ttu-id="34ab7-106">高速シャットダウンが正常に行われるには、MAPI クライアント、MAPI プロバイダー、およびクライアント コンピューターの管理者が高速シャットダウンをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="34ab7-106">For fast shutdown to occur successfully, the MAPI client, MAPI provider, and administrator of the client computer have to support fast shutdown.</span></span> 
  
<span data-ttu-id="34ab7-107">このセクションのトピックでは、クライアントが高速シャットダウンを実行するための MAPI サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="34ab7-107">The topics in this section describe MAPI support for a client to perform fast shutdown.</span></span>
  
[<span data-ttu-id="34ab7-108">高速シャットダウンの概要</span><span class="sxs-lookup"><span data-stu-id="34ab7-108">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
  
> <span data-ttu-id="34ab7-109">このトピックでは、高速シャットダウンの基本的なメカニズムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="34ab7-109">This topic introduces the basic mechanism of fast shutdown.</span></span>
    
[<span data-ttu-id="34ab7-110">Fast Shutdown User Options</span><span class="sxs-lookup"><span data-stu-id="34ab7-110">Fast Shutdown User Options</span></span>](fast-shutdown-user-options.md)
  
> <span data-ttu-id="34ab7-111">このトピックでは、管理者がユーザーの MAPI クライアントのユーザー レベルで高速シャットダウンを採用できる選択肢について説明します。</span><span class="sxs-lookup"><span data-stu-id="34ab7-111">This topic describes the choices available for administrators to adopt fast shutdown at the user level for the user's MAPI clients.</span></span>
    
[<span data-ttu-id="34ab7-112">高速シャットダウンのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="34ab7-112">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)
  
> <span data-ttu-id="34ab7-113">このトピックでは、MAPI クライアントのシャットダウン中にデータが失われるのを防ぐために、高速シャットダウン インターフェイスを使用するベスト プラクティスを推奨します。</span><span class="sxs-lookup"><span data-stu-id="34ab7-113">This topic recommends best practices to use the fast shutdown interfaces to help prevent data loss during a MAPI client shutdown.</span></span>
    

