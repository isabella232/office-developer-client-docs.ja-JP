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
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328008"
---
# <a name="ftaddft"></a><span data-ttu-id="fa68d-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="fa68d-103">FtAddFt</span></span>

  
  
<span data-ttu-id="fa68d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa68d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa68d-105">符号なしの64ビットの整数をもう1つ追加します。</span><span class="sxs-lookup"><span data-stu-id="fa68d-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa68d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fa68d-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa68d-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="fa68d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fa68d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="fa68d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa68d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa68d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa68d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="fa68d-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa68d-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="fa68d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="fa68d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fa68d-112">Parameters</span></span>

 <span data-ttu-id="fa68d-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="fa68d-113">_Addend1_</span></span>
  
> <span data-ttu-id="fa68d-114">順番追加する最初の未署名の64ビット整数を含む[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="fa68d-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="fa68d-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="fa68d-115">_Addend2_</span></span>
  
> <span data-ttu-id="fa68d-116">順番追加する2番目の符号なし64ビット整数を含む**FILETIME**構造。</span><span class="sxs-lookup"><span data-stu-id="fa68d-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa68d-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa68d-117">Return value</span></span>

<span data-ttu-id="fa68d-118">**ftaddft**関数は、2つの整数の合計を含む**FILETIME**構造を返します。</span><span class="sxs-lookup"><span data-stu-id="fa68d-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="fa68d-119">2つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="fa68d-119">The two input parameters remain unchanged.</span></span> 
  

