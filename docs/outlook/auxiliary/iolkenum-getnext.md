---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: 列挙子の次のアカウントを取得します。
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405990"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="a31a6-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="a31a6-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="a31a6-104">列挙子の次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="a31a6-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a31a6-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a31a6-105">Quick info</span></span>

<span data-ttu-id="a31a6-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a31a6-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="a31a6-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a31a6-107">Parameters</span></span>

<span data-ttu-id="a31a6-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="a31a6-108">_ppunk_</span></span>
  
> <span data-ttu-id="a31a6-109">順番[IOlkAccount](iolkaccount.md)インターフェイスを取得するためにクライアントが照会できる**IUnknown**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a31a6-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a31a6-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="a31a6-110">Return values</span></span>

|<span data-ttu-id="a31a6-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="a31a6-111">**HRESULT**</span></span>|<span data-ttu-id="a31a6-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="a31a6-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a31a6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a31a6-113">S_OK</span></span>  <br/> |<span data-ttu-id="a31a6-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="a31a6-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a31a6-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a31a6-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="a31a6-116">列挙子が最後に到達しました。</span><span class="sxs-lookup"><span data-stu-id="a31a6-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a31a6-117">注釈</span><span class="sxs-lookup"><span data-stu-id="a31a6-117">Remarks</span></span>

<span data-ttu-id="a31a6-118">*ppunk*で指定されたインターフェイスは、 **IUnknown**から継承します。</span><span class="sxs-lookup"><span data-stu-id="a31a6-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="a31a6-119">クライアントは、( **IUnknown:: QueryInterface**を使用して) このインターフェイスを照会して、 **IOlkAccount**インターフェイスへのポインターを取得し、このアカウントの情報を取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="a31a6-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a31a6-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a31a6-120">See also</span></span>

- [<span data-ttu-id="a31a6-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="a31a6-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="a31a6-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="a31a6-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="a31a6-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="a31a6-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="a31a6-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="a31a6-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

