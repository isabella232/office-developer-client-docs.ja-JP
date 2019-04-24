---
title: ixpprovider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0aa77ced9d0c242dcafb84ca1e1a60d02db9504a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357450"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="d0d7c-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0d7c-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="d0d7c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0d7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0d7c-105">トランスポートプロバイダオブジェクトを初期化し、不要になったオブジェクトをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="d0d7c-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0d7c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0d7c-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="d0d7c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d0d7c-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d0d7c-109">トランスポート プロバイダーのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d0d7c-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="d0d7c-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0d7c-111">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d0d7c-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d0d7c-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-112">Called by:</span></span>  <br/> |<span data-ttu-id="d0d7c-113">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="d0d7c-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="d0d7c-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d0d7c-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="d0d7c-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="d0d7c-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="d0d7c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d0d7c-117">lpxprovider</span><span class="sxs-lookup"><span data-stu-id="d0d7c-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d0d7c-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="d0d7c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d0d7c-119">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="d0d7c-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="d0d7c-120">トランスポートプロバイダーを正しい順序で閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0d7c-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="d0d7c-121">transportlogon</span><span class="sxs-lookup"><span data-stu-id="d0d7c-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="d0d7c-122">クライアントアプリケーションがトランスポートプロバイダーにログオンするセッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="d0d7c-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

