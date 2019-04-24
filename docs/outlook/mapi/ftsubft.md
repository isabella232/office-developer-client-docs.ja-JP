---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300393"
---
# <a name="ftsubft"></a><span data-ttu-id="0f553-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="0f553-103">FtSubFt</span></span>

  
  
<span data-ttu-id="0f553-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f553-105">1つの符号なし64ビット整数を別の値に減算します。</span><span class="sxs-lookup"><span data-stu-id="0f553-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f553-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0f553-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f553-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="0f553-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0f553-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0f553-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f553-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f553-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f553-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0f553-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f553-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="0f553-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="0f553-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f553-112">Parameters</span></span>

 <span data-ttu-id="0f553-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="0f553-113">_Minuend_</span></span>
  
> <span data-ttu-id="0f553-114">順番_Subtrahend_パラメーターの値を減算する、符号なしの64ビットの整数を含む[FILETIME](filetime.md)構造。</span><span class="sxs-lookup"><span data-stu-id="0f553-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="0f553-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="0f553-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="0f553-116">順番_Minuend_パラメーターによって指定された値から減算される、符号なしの64ビット整数を含む**FILETIME**構造。</span><span class="sxs-lookup"><span data-stu-id="0f553-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0f553-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f553-117">Return value</span></span>

<span data-ttu-id="0f553-118">**ftsubft**関数は、減算の結果を含む**FILETIME**構造を返します。</span><span class="sxs-lookup"><span data-stu-id="0f553-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="0f553-119">2つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0f553-119">The two input parameters remain unchanged.</span></span> 
  

