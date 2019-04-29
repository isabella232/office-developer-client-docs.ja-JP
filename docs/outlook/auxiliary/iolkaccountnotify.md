---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412500"
---
# <a name="iolkaccountnotify"></a><span data-ttu-id="9f673-102">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="9f673-102">IOlkAccountNotify</span></span>

<span data-ttu-id="9f673-103">アカウントの変更についてクライアントへのコールバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f673-103">Provides a callback to the client for changes to an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9f673-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9f673-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f673-105">継承元:</span><span class="sxs-lookup"><span data-stu-id="9f673-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="9f673-106">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="9f673-106">IOlkErrorUnknown</span></span>](iolkerrorunknown.md) <br/> |
|<span data-ttu-id="9f673-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="9f673-107">Provided by:</span></span>  <br/> | <span data-ttu-id="9f673-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="9f673-108">Client</span></span>  <br/> |
|<span data-ttu-id="9f673-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="9f673-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9f673-110">IID_IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="9f673-110">IID_IOlkAccountNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9f673-111">v の順序</span><span class="sxs-lookup"><span data-stu-id="9f673-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9f673-112">Notify</span><span class="sxs-lookup"><span data-stu-id="9f673-112">Notify</span></span>](iolkaccountnotify-notify.md) <br/> |<span data-ttu-id="9f673-113">指定したアカウントへの変更をクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="9f673-113">Notifies the client of changes to the specified account.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f673-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9f673-114">Remarks</span></span>

<span data-ttu-id="9f673-115">このインターフェイスは、通知を設定するときに[IOlkAccountManager:: アドバイズ](iolkaccountmanager-advise.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="9f673-115">This interface is passed to [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) when setting up notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f673-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f673-116">See also</span></span>

- [<span data-ttu-id="9f673-117">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="9f673-117">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="9f673-118">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="9f673-118">Constants (Account management API)</span></span>](constants-account-management-api.md)

