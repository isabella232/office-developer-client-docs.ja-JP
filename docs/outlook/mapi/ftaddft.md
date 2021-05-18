---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404765"
---
# <a name="ftaddft"></a><span data-ttu-id="e20f2-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="e20f2-103">FtAddFt</span></span>

  
  
<span data-ttu-id="e20f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e20f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e20f2-105">1 つの符号なし 64 ビット整数を別の整数に追加します。</span><span class="sxs-lookup"><span data-stu-id="e20f2-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e20f2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e20f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="e20f2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e20f2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e20f2-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e20f2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e20f2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e20f2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e20f2-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e20f2-110">Called by:</span></span>  <br/> |<span data-ttu-id="e20f2-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e20f2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="e20f2-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e20f2-112">Parameters</span></span>

 <span data-ttu-id="e20f2-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="e20f2-113">_Addend1_</span></span>
  
> <span data-ttu-id="e20f2-114">[in]追加 [する最初](filetime.md) の符号なし 64 ビット整数を含む FILETIME 構造体。</span><span class="sxs-lookup"><span data-stu-id="e20f2-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="e20f2-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="e20f2-115">_Addend2_</span></span>
  
> <span data-ttu-id="e20f2-116">[in]追加 **する 2** 番目の符号なし 64 ビット整数を含む FILETIME 構造体。</span><span class="sxs-lookup"><span data-stu-id="e20f2-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e20f2-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="e20f2-117">Return value</span></span>

<span data-ttu-id="e20f2-118">**FtAddFt** 関数は、2 つの整数の合計を含む **FILETIME** 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="e20f2-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="e20f2-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="e20f2-119">The two input parameters remain unchanged.</span></span> 
  

