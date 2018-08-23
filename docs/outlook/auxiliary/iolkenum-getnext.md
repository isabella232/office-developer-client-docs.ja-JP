---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: 列挙子では、次のアカウントを取得します。
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799507"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="b427e-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="b427e-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="b427e-104">列挙子では、次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="b427e-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b427e-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b427e-105">Quick info</span></span>

<span data-ttu-id="b427e-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b427e-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="b427e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b427e-107">Parameters</span></span>

<span data-ttu-id="b427e-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="b427e-108">_ppunk_</span></span>
  
> <span data-ttu-id="b427e-109">[in][IOlkAccount](iolkaccount.md)インターフェイスを取得するのには、クライアントが照会できる**IUnknown**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b427e-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b427e-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b427e-110">Return values</span></span>

|<span data-ttu-id="b427e-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="b427e-111">**HRESULT**</span></span>|<span data-ttu-id="b427e-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="b427e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b427e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b427e-113">S_OK</span></span>  <br/> |<span data-ttu-id="b427e-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="b427e-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b427e-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b427e-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="b427e-116">列挙子には、末尾に到達します。</span><span class="sxs-lookup"><span data-stu-id="b427e-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b427e-117">注釈</span><span class="sxs-lookup"><span data-stu-id="b427e-117">Remarks</span></span>

<span data-ttu-id="b427e-118">*Ppunk*によって指定されたインターフェイスは、 **IUnknown**から継承します。</span><span class="sxs-lookup"><span data-stu-id="b427e-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="b427e-119">クライアントは、 **IOlkAccount**インターフェイスへのポインターを取得する ( **IUnknown::QueryInterface**を使用して) このインターフェイスを問い合わせることができますを取得したり、このアカウントの情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="b427e-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b427e-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="b427e-120">See also</span></span>

- [<span data-ttu-id="b427e-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="b427e-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="b427e-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="b427e-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="b427e-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="b427e-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="b427e-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="b427e-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

