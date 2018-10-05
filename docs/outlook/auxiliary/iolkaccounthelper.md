---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386412"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="11636-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="11636-102">IOlkAccountHelper</span></span>

<span data-ttu-id="11636-103">アカウントを管理する現在の MAPI セッションでは、ヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="11636-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="11636-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="11636-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11636-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="11636-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="11636-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="11636-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="11636-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="11636-107">Provided by:</span></span>  <br/> |<span data-ttu-id="11636-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="11636-108">Client</span></span>  <br/> |
|<span data-ttu-id="11636-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="11636-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="11636-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="11636-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="11636-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="11636-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="11636-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="11636-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="11636-113">*このメンバーは、プレース ホルダーではサポートされていません。*</span><span class="sxs-lookup"><span data-stu-id="11636-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="11636-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="11636-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="11636-115">アカウントのプロファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="11636-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="11636-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="11636-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="11636-117">MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="11636-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="11636-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="11636-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="11636-119">[IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="11636-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11636-120">備考</span><span class="sxs-lookup"><span data-stu-id="11636-120">Remarks</span></span>

<span data-ttu-id="11636-121">このインターフェイスは、アカウント マネージャーを初期化するときに、 [IOlkAccountManager::Init](iolkaccountmanager-init.md)に渡されます。</span><span class="sxs-lookup"><span data-stu-id="11636-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11636-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="11636-122">See also</span></span>

- [<span data-ttu-id="11636-123">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="11636-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="11636-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="11636-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

