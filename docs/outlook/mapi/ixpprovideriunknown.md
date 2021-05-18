---
title: IXPProvider IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0aa77ced9d0c242dcafb84ca1e1a60d02db9504a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404695"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="b85ed-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b85ed-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="b85ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b85ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b85ed-105">トランスポート プロバイダー オブジェクトを初期化し、不要になったときにオブジェクトをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="b85ed-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b85ed-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b85ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="b85ed-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="b85ed-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="b85ed-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b85ed-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b85ed-109">トランスポート プロバイダーのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b85ed-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="b85ed-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="b85ed-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b85ed-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b85ed-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="b85ed-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b85ed-112">Called by:</span></span>  <br/> |<span data-ttu-id="b85ed-113">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="b85ed-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="b85ed-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="b85ed-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b85ed-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="b85ed-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="b85ed-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="b85ed-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b85ed-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="b85ed-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b85ed-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b85ed-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b85ed-119">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="b85ed-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="b85ed-120">トランスポート プロバイダーを順番に閉じます。</span><span class="sxs-lookup"><span data-stu-id="b85ed-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="b85ed-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="b85ed-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="b85ed-122">クライアント アプリケーションがトランスポート プロバイダーにログオンするセッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="b85ed-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

