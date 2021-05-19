---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: IOlkAccountHelper::GetMapiSession によって返された MAPI セッション オブジェクトを解放します。
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418632"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="dec23-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="dec23-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="dec23-104">[IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="dec23-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dec23-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="dec23-105">Quick info</span></span>

<span data-ttu-id="dec23-106">[「IOlkAccountHelper」を参照してください](iolkaccounthelper.md)。</span><span class="sxs-lookup"><span data-stu-id="dec23-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="dec23-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="dec23-107">Return values</span></span>

|<span data-ttu-id="dec23-108">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="dec23-108">**HRESULT**</span></span>|<span data-ttu-id="dec23-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="dec23-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dec23-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dec23-110">S_OK</span></span>  <br/> |<span data-ttu-id="dec23-111">**IOlkAccountHelper** の実装で **、IOlkAccountHelper::GetMapiSession** で返される独自の MAPI セッションを作成する場合は、ここでセッションを解放し、S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dec23-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="dec23-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="dec23-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="dec23-113">**IOlkAccountHelper** の実装で独自の MAPI セッションが作成されていない場合は、その MAPI セッションのみをE_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="dec23-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="dec23-114">この場合、サポートされている戻り値はこれが唯一です。</span><span class="sxs-lookup"><span data-stu-id="dec23-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dec23-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="dec23-115">See also</span></span>

- [<span data-ttu-id="dec23-116">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="dec23-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="dec23-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="dec23-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

