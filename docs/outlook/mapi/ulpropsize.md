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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416903"
---
# <a name="ulpropsize"></a><span data-ttu-id="27abb-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="27abb-103">UlPropSize</span></span>

  
  
<span data-ttu-id="27abb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27abb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27abb-105">1つのプロパティ値のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="27abb-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27abb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="27abb-106">Header file:</span></span>  <br/> |<span data-ttu-id="27abb-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27abb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="27abb-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="27abb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27abb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27abb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27abb-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="27abb-110">Called by:</span></span>  <br/> |<span data-ttu-id="27abb-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="27abb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="27abb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27abb-112">Parameters</span></span>

 <span data-ttu-id="27abb-113">_lpspropvalue_</span><span class="sxs-lookup"><span data-stu-id="27abb-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="27abb-114">順番測定するプロパティを定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="27abb-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27abb-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="27abb-115">Return value</span></span>

<span data-ttu-id="27abb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="27abb-116">S_OK</span></span> 
  
> <span data-ttu-id="27abb-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="27abb-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="27abb-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="27abb-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="27abb-119">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="27abb-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27abb-120">注釈</span><span class="sxs-lookup"><span data-stu-id="27abb-120">Remarks</span></span>

<span data-ttu-id="27abb-121">**ulpropsize**関数は、指定されたプロパティのプロパティ値のサイズをバイト単位で返します。</span><span class="sxs-lookup"><span data-stu-id="27abb-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="27abb-122">**spropvalue**構造の残りの部分のサイズは無視されます。</span><span class="sxs-lookup"><span data-stu-id="27abb-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

