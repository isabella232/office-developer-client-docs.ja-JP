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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592025"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="68b31-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="68b31-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="68b31-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68b31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68b31-105">別の 1 つの符号なし 32 ビット整数を乗算します。</span><span class="sxs-lookup"><span data-stu-id="68b31-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68b31-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="68b31-106">Header file:</span></span>  <br/> |<span data-ttu-id="68b31-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="68b31-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="68b31-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="68b31-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="68b31-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="68b31-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="68b31-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="68b31-110">Called by:</span></span>  <br/> |<span data-ttu-id="68b31-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="68b31-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="68b31-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68b31-112">Parameters</span></span>

 <span data-ttu-id="68b31-113">_被乗数_</span><span class="sxs-lookup"><span data-stu-id="68b31-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="68b31-114">[in]_乗数_パラメーターの値が乗算されます符号なし 32 ビット整数を含むダブル ワード。</span><span class="sxs-lookup"><span data-stu-id="68b31-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="68b31-115">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="68b31-115">_Multiplier_</span></span>
  
> <span data-ttu-id="68b31-116">[in]マルチ プライアで 32 ビットの符号なし整数を含むダブル ワード。</span><span class="sxs-lookup"><span data-stu-id="68b31-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68b31-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="68b31-117">Return value</span></span>

<span data-ttu-id="68b31-118">**FtMulDwDw**関数は、2 つの整数の積を格納する[FILETIME](filetime.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="68b31-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="68b31-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="68b31-119">The two input parameters remain unchanged.</span></span> 
  

