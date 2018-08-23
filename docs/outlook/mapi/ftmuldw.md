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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583996"
---
# <a name="ftmuldw"></a><span data-ttu-id="a9a19-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="a9a19-103">FtMulDw</span></span>

  
  
<span data-ttu-id="a9a19-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9a19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9a19-105">32 ビットの符号なし整数を符号なしの 64 ビット整数を乗算します。</span><span class="sxs-lookup"><span data-stu-id="a9a19-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9a19-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a9a19-106">Header file:</span></span>  <br/> |<span data-ttu-id="a9a19-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a9a19-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a9a19-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a9a19-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a9a19-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a9a19-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a9a19-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9a19-110">Called by:</span></span>  <br/> |<span data-ttu-id="a9a19-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a9a19-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="a9a19-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9a19-112">Parameters</span></span>

 <span data-ttu-id="a9a19-113">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="a9a19-113">_Multiplier_</span></span>
  
> <span data-ttu-id="a9a19-114">[in]マルチ プライアで 32 ビットの符号なし整数を含むダブル ワード。</span><span class="sxs-lookup"><span data-stu-id="a9a19-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="a9a19-115">_被乗数_</span><span class="sxs-lookup"><span data-stu-id="a9a19-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="a9a19-116">[in]_乗数_パラメーターの値が乗算されます、64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="a9a19-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a9a19-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a9a19-117">Return value</span></span>

<span data-ttu-id="a9a19-118">**FtMulDw**関数は、2 つの整数の積を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a9a19-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="a9a19-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a9a19-119">The two input parameters remain unchanged.</span></span> 
  

