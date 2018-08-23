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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800143"
---
# <a name="ftaddft"></a><span data-ttu-id="871bb-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="871bb-103">FtAddFt</span></span>

  
  
<span data-ttu-id="871bb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="871bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="871bb-105">別の 1 つの符号なし 64 ビット整数を追加します。</span><span class="sxs-lookup"><span data-stu-id="871bb-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="871bb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="871bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="871bb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="871bb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="871bb-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="871bb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="871bb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="871bb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="871bb-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="871bb-110">Called by:</span></span>  <br/> |<span data-ttu-id="871bb-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="871bb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="871bb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="871bb-112">Parameters</span></span>

 <span data-ttu-id="871bb-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="871bb-113">_Addend1_</span></span>
  
> <span data-ttu-id="871bb-114">[in]追加する最初の符号なし 64 ビット整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="871bb-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="871bb-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="871bb-115">_Addend2_</span></span>
  
> <span data-ttu-id="871bb-116">[in]追加する 2 番目の符号なし 64 ビット整数を格納する**FILETIME**構造体。</span><span class="sxs-lookup"><span data-stu-id="871bb-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="871bb-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="871bb-117">Return value</span></span>

<span data-ttu-id="871bb-118">**FtAddFt**関数は、2 つの整数の合計を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="871bb-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="871bb-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="871bb-119">The two input parameters remain unchanged.</span></span> 
  

