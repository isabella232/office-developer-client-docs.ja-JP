---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406347"
---
# <a name="ftmuldw"></a><span data-ttu-id="cde2c-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="cde2c-103">FtMulDw</span></span>

  
  
<span data-ttu-id="cde2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cde2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cde2c-105">符号なしの64ビット整数を、符号なしの32ビット整数で乗算します。</span><span class="sxs-lookup"><span data-stu-id="cde2c-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cde2c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cde2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="cde2c-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="cde2c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cde2c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cde2c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cde2c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cde2c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cde2c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cde2c-110">Called by:</span></span>  <br/> |<span data-ttu-id="cde2c-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="cde2c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="cde2c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cde2c-112">Parameters</span></span>

 <span data-ttu-id="cde2c-113">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="cde2c-113">_Multiplier_</span></span>
  
> <span data-ttu-id="cde2c-114">順番符号なし32ビットの整数乗数を含む二重の単語。</span><span class="sxs-lookup"><span data-stu-id="cde2c-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="cde2c-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="cde2c-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="cde2c-116">順番_乗数_パラメーターの値で乗算する、符号なしの64ビット整数を含む[FILETIME](filetime.md)構造。</span><span class="sxs-lookup"><span data-stu-id="cde2c-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cde2c-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="cde2c-117">Return value</span></span>

<span data-ttu-id="cde2c-118">**FtMulDw**関数は、2つの整数の積を含む**FILETIME**構造を返します。</span><span class="sxs-lookup"><span data-stu-id="cde2c-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="cde2c-119">2つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="cde2c-119">The two input parameters remain unchanged.</span></span> 
  

