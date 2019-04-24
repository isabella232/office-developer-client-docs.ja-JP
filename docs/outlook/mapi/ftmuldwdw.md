---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327980"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="598a8-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="598a8-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="598a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="598a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="598a8-105">1つの符号なし32ビット整数を別の数値で乗算します。</span><span class="sxs-lookup"><span data-stu-id="598a8-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="598a8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="598a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="598a8-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="598a8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="598a8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="598a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="598a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="598a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="598a8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="598a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="598a8-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="598a8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="598a8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="598a8-112">Parameters</span></span>

 <span data-ttu-id="598a8-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="598a8-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="598a8-114">順番_乗数_パラメーターの値で乗算する、符号なしの32ビット整数を含む二重の単語。</span><span class="sxs-lookup"><span data-stu-id="598a8-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="598a8-115">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="598a8-115">_Multiplier_</span></span>
  
> <span data-ttu-id="598a8-116">順番符号なし32ビットの整数乗数を含む二重の単語。</span><span class="sxs-lookup"><span data-stu-id="598a8-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="598a8-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="598a8-117">Return value</span></span>

<span data-ttu-id="598a8-118">**FtMulDwDw**関数は、2つの整数の積を含む[FILETIME](filetime.md)構造を返します。</span><span class="sxs-lookup"><span data-stu-id="598a8-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="598a8-119">2つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="598a8-119">The two input parameters remain unchanged.</span></span> 
  

