---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804151"
---
# <a name="ulpropsize"></a><span data-ttu-id="e6c2c-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="e6c2c-103">UlPropSize</span></span>

  
  
<span data-ttu-id="e6c2c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6c2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6c2c-105">1 つのプロパティの値のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6c2c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e6c2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6c2c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6c2c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e6c2c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6c2c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c2c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6c2c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6c2c-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e6c2c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="e6c2c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6c2c-112">Parameters</span></span>

 <span data-ttu-id="e6c2c-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="e6c2c-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="e6c2c-114">[in]測定するプロパティを定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6c2c-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e6c2c-115">Return value</span></span>

<span data-ttu-id="e6c2c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6c2c-116">S_OK</span></span> 
  
> <span data-ttu-id="e6c2c-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e6c2c-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e6c2c-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e6c2c-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e6c2c-119">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6c2c-120">備考</span><span class="sxs-lookup"><span data-stu-id="e6c2c-120">Remarks</span></span>

<span data-ttu-id="e6c2c-121">**UlPropSize**関数は、指定されたプロパティのプロパティ値のバイト単位のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="e6c2c-122">**SPropValue**構造体の残りの部分のサイズを無視します。</span><span class="sxs-lookup"><span data-stu-id="e6c2c-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

