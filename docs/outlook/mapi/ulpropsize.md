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
# <a name="ulpropsize"></a><span data-ttu-id="e9974-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="e9974-103">UlPropSize</span></span>

  
  
<span data-ttu-id="e9974-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9974-105">1 つのプロパティ値のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="e9974-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9974-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9974-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9974-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9974-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e9974-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e9974-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9974-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e9974-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e9974-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e9974-110">Called by:</span></span>  <br/> |<span data-ttu-id="e9974-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9974-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="e9974-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9974-112">Parameters</span></span>

 <span data-ttu-id="e9974-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="e9974-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="e9974-114">[in]測定するプロパティを定義する [SPropValue](spropvalue.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9974-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9974-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9974-115">Return value</span></span>

<span data-ttu-id="e9974-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9974-116">S_OK</span></span> 
  
> <span data-ttu-id="e9974-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e9974-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e9974-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e9974-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e9974-119">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="e9974-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9974-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e9974-120">Remarks</span></span>

<span data-ttu-id="e9974-121">**UlPropSize** 関数は、指定したプロパティのプロパティ値のサイズをバイト単位で返します。</span><span class="sxs-lookup"><span data-stu-id="e9974-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="e9974-122">SPropValue 構造体の残りのサイズ **は無視** されます。</span><span class="sxs-lookup"><span data-stu-id="e9974-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

