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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321897"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="06416-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="06416-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="06416-104">列挙子の次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="06416-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="06416-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="06416-105">Quick info</span></span>

<span data-ttu-id="06416-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06416-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="06416-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06416-107">Parameters</span></span>

<span data-ttu-id="06416-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="06416-108">_ppunk_</span></span>
  
> <span data-ttu-id="06416-109">順番[IOlkAccount](iolkaccount.md)インターフェイスを取得するためにクライアントが照会できる**IUnknown**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="06416-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="06416-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="06416-110">Return values</span></span>

|<span data-ttu-id="06416-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="06416-111">**HRESULT**</span></span>|<span data-ttu-id="06416-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="06416-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06416-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="06416-113">S_OK</span></span>  <br/> |<span data-ttu-id="06416-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="06416-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="06416-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="06416-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="06416-116">列挙子が最後に到達しました。</span><span class="sxs-lookup"><span data-stu-id="06416-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06416-117">解説</span><span class="sxs-lookup"><span data-stu-id="06416-117">Remarks</span></span>

<span data-ttu-id="06416-118">*ppunk*で指定されたインターフェイスは、 **IUnknown**から継承します。</span><span class="sxs-lookup"><span data-stu-id="06416-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="06416-119">クライアントは、( **IUnknown:: QueryInterface**を使用して) このインターフェイスを照会して、 **IOlkAccount**インターフェイスへのポインターを取得し、このアカウントの情報を取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="06416-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06416-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="06416-120">See also</span></span>

- [<span data-ttu-id="06416-121">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="06416-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="06416-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="06416-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="06416-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="06416-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="06416-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="06416-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

