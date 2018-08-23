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
ms.openlocfilehash: 49cb500279540317059cde2d9baba28fcbf06165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574112"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="ea0c4-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea0c4-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="ea0c4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea0c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea0c4-105">トランスポート プロバイダーのオブジェクトを初期化し、不要になったときに、オブジェクトをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea0c4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ea0c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea0c4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ea0c4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ea0c4-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ea0c4-109">トランスポート プロバイダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ea0c4-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="ea0c4-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ea0c4-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ea0c4-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="ea0c4-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-112">Called by:</span></span>  <br/> |<span data-ttu-id="ea0c4-113">MAPI スプーラーを無効</span><span class="sxs-lookup"><span data-stu-id="ea0c4-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="ea0c4-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ea0c4-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="ea0c4-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="ea0c4-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ea0c4-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="ea0c4-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ea0c4-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ea0c4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ea0c4-119">シャットダウン</span><span class="sxs-lookup"><span data-stu-id="ea0c4-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="ea0c4-120">適切な順序でトランスポート プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="ea0c4-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="ea0c4-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="ea0c4-122">クライアント アプリケーションへのログオンに、トランスポート プロバイダーのセッションを確立します。</span><span class="sxs-lookup"><span data-stu-id="ea0c4-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

