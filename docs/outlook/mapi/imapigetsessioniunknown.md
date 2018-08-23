---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 17c9a7ba54d7dd0b4d97c06f6343e563223f8100
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800595"
---
# <a name="imapigetsession--iunknown"></a><span data-ttu-id="06a65-103">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06a65-103">IMAPIGetSession : IUnknown</span></span>

  
  
<span data-ttu-id="06a65-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06a65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06a65-105">サポート オブジェクトに関連付けられている現在の MAPI セッションへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="06a65-105">Provides access to the current MAPI session associated with the support object.</span></span> <span data-ttu-id="06a65-106">MAPI プロバイダーには、このインターフェイスは、MAPI のサポート オブジェクトを照会できます。</span><span class="sxs-lookup"><span data-stu-id="06a65-106">MAPI Providers can query their MAPI Support Object for this interface.</span></span> <span data-ttu-id="06a65-107">サポート オブジェクトの詳細については、[オブジェクトのサポートの概要](support-object-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a65-107">For more information on support objects, see [Support Object Overview](support-object-overview.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06a65-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="06a65-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="06a65-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="06a65-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="06a65-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="06a65-110">Called by:</span></span>  <br/> |<span data-ttu-id="06a65-111">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="06a65-111">MAPI Providers</span></span>  <br/> |
|<span data-ttu-id="06a65-112">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="06a65-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="06a65-113">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="06a65-113">IID_IMAPIGetSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="06a65-114">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="06a65-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="06a65-115">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="06a65-115">GetMAPISession</span></span>](imapigetsession-getmapisession.md) <br/> |<span data-ttu-id="06a65-116">現在の MAPI セッションへのポインターを取得すると呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="06a65-116">Called to obtain a pointer to the current MAPI session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06a65-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="06a65-117">See also</span></span>



[<span data-ttu-id="06a65-118">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="06a65-118">GetMAPISession</span></span>](imapigetsession-getmapisession.md)
  
[<span data-ttu-id="06a65-119">IMAPISupport</span><span class="sxs-lookup"><span data-stu-id="06a65-119">IMAPISupport</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="06a65-120">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="06a65-120">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="06a65-121">サポート オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="06a65-121">Support Object Overview</span></span>](support-object-overview.md)

