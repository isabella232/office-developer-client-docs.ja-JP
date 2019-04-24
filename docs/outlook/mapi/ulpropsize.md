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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315303"
---
# <a name="ulpropsize"></a><span data-ttu-id="a8c7c-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="a8c7c-103">UlPropSize</span></span>

  
  
<span data-ttu-id="a8c7c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c7c-105">1つのプロパティ値のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="a8c7c-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c7c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a8c7c-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8c7c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8c7c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8c7c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a8c7c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8c7c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8c7c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8c7c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a8c7c-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8c7c-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="a8c7c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="a8c7c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a8c7c-112">Parameters</span></span>

 <span data-ttu-id="a8c7c-113">_lpspropvalue_</span><span class="sxs-lookup"><span data-stu-id="a8c7c-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="a8c7c-114">順番測定するプロパティを定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a8c7c-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8c7c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="a8c7c-115">Return value</span></span>

<span data-ttu-id="a8c7c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8c7c-116">S_OK</span></span> 
  
> <span data-ttu-id="a8c7c-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a8c7c-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a8c7c-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="a8c7c-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="a8c7c-119">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="a8c7c-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8c7c-120">解説</span><span class="sxs-lookup"><span data-stu-id="a8c7c-120">Remarks</span></span>

<span data-ttu-id="a8c7c-121">**ulpropsize**関数は、指定されたプロパティのプロパティ値のサイズをバイト単位で返します。</span><span class="sxs-lookup"><span data-stu-id="a8c7c-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="a8c7c-122">**spropvalue**構造の残りの部分のサイズは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a8c7c-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

