---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: IOlkAccountHelper::GetMapiSession によって返された MAPI セッション オブジェクトを解放します。
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799458"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="99c8d-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="99c8d-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="99c8d-104">- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="99c8d-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="99c8d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="99c8d-105">Quick info</span></span>

<span data-ttu-id="99c8d-106">[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99c8d-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="99c8d-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="99c8d-107">Return values</span></span>

|<span data-ttu-id="99c8d-108">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="99c8d-108">**HRESULT**</span></span>|<span data-ttu-id="99c8d-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="99c8d-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99c8d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="99c8d-110">S_OK</span></span>  <br/> |<span data-ttu-id="99c8d-111">**IOlkAccountHelper**の実装では、 **IOlkAccountHelper::GetMapiSession**で返される、独自の MAPI セッションを作成する場合は、ここでは、セッションを解放してと S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c8d-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="99c8d-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="99c8d-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="99c8d-113">**IOlkAccountHelper**の実装では、独自の MAPI セッションを作成しなかった場合のみ E_NOTIMPL を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c8d-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="99c8d-114">この例では、これは、戻り値はサポートされているだけです。</span><span class="sxs-lookup"><span data-stu-id="99c8d-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99c8d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="99c8d-115">See also</span></span>

- [<span data-ttu-id="99c8d-116">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="99c8d-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="99c8d-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="99c8d-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

