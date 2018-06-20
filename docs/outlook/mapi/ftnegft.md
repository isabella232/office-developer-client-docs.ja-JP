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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800151"
---
# <a name="ftnegft"></a><span data-ttu-id="7b71c-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="7b71c-103">FtNegFt</span></span>

  
  
<span data-ttu-id="7b71c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b71c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b71c-105">64 ビットの符号なし整数の 2 の補数を計算します。</span><span class="sxs-lookup"><span data-stu-id="7b71c-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b71c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7b71c-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b71c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7b71c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7b71c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7b71c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b71c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b71c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b71c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7b71c-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b71c-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7b71c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="7b71c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b71c-112">Parameters</span></span>

 <span data-ttu-id="7b71c-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="7b71c-113">_ft_</span></span>
  
> <span data-ttu-id="7b71c-114">[in]2 の補数を計算する対象の 64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="7b71c-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b71c-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7b71c-115">Return value</span></span>

<span data-ttu-id="7b71c-116">**FtNegFt**関数は、整数の 2 の補数を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="7b71c-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="7b71c-117">入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7b71c-117">The input parameter remains unchanged.</span></span> 
  

