---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322156"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="79638-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="79638-102">IOlkAccountHelper</span></span>

<span data-ttu-id="79638-103">現在の MAPI セッションでアカウントを管理するためのヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="79638-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79638-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="79638-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79638-105">継承元:</span><span class="sxs-lookup"><span data-stu-id="79638-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="79638-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="79638-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="79638-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="79638-107">Provided by:</span></span>  <br/> |<span data-ttu-id="79638-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="79638-108">Client</span></span>  <br/> |
|<span data-ttu-id="79638-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="79638-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="79638-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="79638-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="79638-111">v の順序</span><span class="sxs-lookup"><span data-stu-id="79638-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="79638-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="79638-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="79638-113">*このメンバーはプレースホルダーで、サポートされていません。*</span><span class="sxs-lookup"><span data-stu-id="79638-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="79638-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="79638-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="79638-115">アカウントのプロファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="79638-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="79638-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="79638-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="79638-117">MAPI セッションを開き、アカウントマネージャーのセッションへの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="79638-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="79638-118">「sosoffsession」</span><span class="sxs-lookup"><span data-stu-id="79638-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="79638-119">[IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッションオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="79638-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79638-120">解説</span><span class="sxs-lookup"><span data-stu-id="79638-120">Remarks</span></span>

<span data-ttu-id="79638-121">このインターフェイスは、アカウントマネージャーを初期化するときに[IOlkAccountManager:: Init](iolkaccountmanager-init.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="79638-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79638-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="79638-122">See also</span></span>

- [<span data-ttu-id="79638-123">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="79638-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="79638-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="79638-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

