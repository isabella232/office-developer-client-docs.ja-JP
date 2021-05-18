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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412913"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="7402e-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="7402e-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="7402e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7402e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7402e-105">1 つの符号なし 32 ビット整数を別の整数で乗算します。</span><span class="sxs-lookup"><span data-stu-id="7402e-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7402e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7402e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7402e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7402e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7402e-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="7402e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7402e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7402e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7402e-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7402e-110">Called by:</span></span>  <br/> |<span data-ttu-id="7402e-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7402e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="7402e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7402e-112">Parameters</span></span>

 <span data-ttu-id="7402e-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="7402e-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="7402e-114">[in]Multiplier パラメーターの値を乗算する符号なし 32 ビット整数を含む 2 つの  _単語_ 。</span><span class="sxs-lookup"><span data-stu-id="7402e-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="7402e-115">_べき乗_</span><span class="sxs-lookup"><span data-stu-id="7402e-115">_Multiplier_</span></span>
  
> <span data-ttu-id="7402e-116">[in]符号なし 32 ビット整数乗数を含む 2 つの単語。</span><span class="sxs-lookup"><span data-stu-id="7402e-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7402e-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="7402e-117">Return value</span></span>

<span data-ttu-id="7402e-118">**FtMulDwDw** 関数は、2 つの整数の製品を含む [FILETIME](filetime.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="7402e-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="7402e-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7402e-119">The two input parameters remain unchanged.</span></span> 
  

