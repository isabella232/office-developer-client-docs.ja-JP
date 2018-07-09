---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: '最終更新日: 2012 年 2 月 20 日'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801651"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="0cb2e-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="0cb2e-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="0cb2e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0cb2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0cb2e-105">ワイド文字列へのポインターが有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="0cb2e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0cb2e-106">Parameters</span></span>

 <span data-ttu-id="0cb2e-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="0cb2e-107">_lpsz_</span></span>
  
> <span data-ttu-id="0cb2e-108">[in]ワイド文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="0cb2e-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="0cb2e-109">_ucchMax_</span></span>
  
> <span data-ttu-id="0cb2e-110">[in]文字列の終端文字を含む文字の最大長。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0cb2e-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0cb2e-111">Return value</span></span>

<span data-ttu-id="0cb2e-112">ブール値、文字列が無効な場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cb2e-113">備考</span><span class="sxs-lookup"><span data-stu-id="0cb2e-113">Remarks</span></span>

<span data-ttu-id="0cb2e-114">この関数は、 [IsBadStringPtr](http://msdn.microsoft.com/ja-jp/library/aa366714%28VS.85%29.aspx)をラップします。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/ja-jp/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="0cb2e-115">詳細については、 [IsBadStringPtr](http://msdn.microsoft.com/ja-jp/library/aa366714%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0cb2e-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/ja-jp/library/aa366714%28VS.85%29.aspx).</span></span>
  

