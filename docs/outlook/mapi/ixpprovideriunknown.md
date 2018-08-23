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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e12f69e3486e5eeb9087b30753735f7f910dc6f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801280"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="0c58f-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c58f-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="0c58f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c58f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c58f-105">トランスポート プロバイダーのオブジェクトを初期化し、不要になったときに、オブジェクトをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="0c58f-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c58f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c58f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c58f-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="0c58f-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="0c58f-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="0c58f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0c58f-109">トランスポート プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0c58f-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="0c58f-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0c58f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c58f-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0c58f-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="0c58f-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0c58f-112">Called by:</span></span>  <br/> |<span data-ttu-id="0c58f-113">MAPI スプーラーを無効</span><span class="sxs-lookup"><span data-stu-id="0c58f-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="0c58f-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="0c58f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0c58f-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="0c58f-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="0c58f-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="0c58f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0c58f-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="0c58f-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0c58f-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="0c58f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0c58f-119">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="0c58f-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="0c58f-120">適切な順序でトランスポート プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c58f-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="0c58f-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="0c58f-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="0c58f-122">クライアント アプリケーションへのログオンに、トランスポート プロバイダーのセッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="0c58f-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

