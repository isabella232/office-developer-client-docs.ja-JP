---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338466"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="ead46-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="ead46-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="ead46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ead46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ead46-105">指定した Unicode 文字列の長さ (終端の null 文字を除く) を指定します。</span><span class="sxs-lookup"><span data-stu-id="ead46-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="ead46-106">代わりに、 [stringcchlength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="ead46-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="ead46-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ead46-107">Parameters</span></span>

 <span data-ttu-id="ead46-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ead46-108">_lpsz_</span></span>
  
> <span data-ttu-id="ead46-109">順番チェックする null で終了する Unicode 文字列。</span><span class="sxs-lookup"><span data-stu-id="ead46-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ead46-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="ead46-110">Return value</span></span>

<span data-ttu-id="ead46-111">関数は、文字列の長さの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="ead46-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="ead46-112">文字列の文字数で、終端の null 文字は含みません。</span><span class="sxs-lookup"><span data-stu-id="ead46-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="ead46-113">_lpsz_が NULL の場合、この関数は0を返します。</span><span class="sxs-lookup"><span data-stu-id="ead46-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ead46-114">解説</span><span class="sxs-lookup"><span data-stu-id="ead46-114">Remarks</span></span>

<span data-ttu-id="ead46-115">この関数は、 **lstrlen**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="ead46-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="ead46-116">詳細については、「 [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ead46-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ead46-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="ead46-117">See also</span></span>



[<span data-ttu-id="ead46-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="ead46-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="ead46-119">stringcchlength</span><span class="sxs-lookup"><span data-stu-id="ead46-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

