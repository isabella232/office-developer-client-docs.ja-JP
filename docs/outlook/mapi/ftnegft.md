---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423385"
---
# <a name="ftnegft"></a><span data-ttu-id="4fc39-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="4fc39-103">FtNegFt</span></span>

  
  
<span data-ttu-id="4fc39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc39-105">符号なしの64ビット整数の2つの補数を計算します。</span><span class="sxs-lookup"><span data-stu-id="4fc39-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fc39-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4fc39-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fc39-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="4fc39-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4fc39-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="4fc39-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fc39-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc39-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4fc39-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4fc39-110">Called by:</span></span>  <br/> |<span data-ttu-id="4fc39-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4fc39-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="4fc39-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4fc39-112">Parameters</span></span>

 <span data-ttu-id="4fc39-113">_cm_</span><span class="sxs-lookup"><span data-stu-id="4fc39-113">_ft_</span></span>
  
> <span data-ttu-id="4fc39-114">順番2つの補数を計算するための符号なし64ビットの整数を含む[FILETIME](filetime.md)構造。</span><span class="sxs-lookup"><span data-stu-id="4fc39-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4fc39-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="4fc39-115">Return value</span></span>

<span data-ttu-id="4fc39-116">**FtNegFt**関数は、2の整数の補数を含む**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="4fc39-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="4fc39-117">入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="4fc39-117">The input parameter remains unchanged.</span></span> 
  

