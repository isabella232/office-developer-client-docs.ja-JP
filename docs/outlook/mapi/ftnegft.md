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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800151"
---
# <a name="ftnegft"></a><span data-ttu-id="0c708-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="0c708-103">FtNegFt</span></span>

  
  
<span data-ttu-id="0c708-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c708-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c708-105">64 ビットの符号なし整数の 2 の補数を計算します。</span><span class="sxs-lookup"><span data-stu-id="0c708-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c708-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c708-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c708-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0c708-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0c708-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0c708-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c708-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c708-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c708-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0c708-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c708-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0c708-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="0c708-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c708-112">Parameters</span></span>

 <span data-ttu-id="0c708-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="0c708-113">_ft_</span></span>
  
> <span data-ttu-id="0c708-114">[in]2 の補数を計算する対象の 64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="0c708-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c708-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="0c708-115">Return value</span></span>

<span data-ttu-id="0c708-116">**FtNegFt**関数は、整数の 2 の補数を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="0c708-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="0c708-117">入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0c708-117">The input parameter remains unchanged.</span></span> 
  

