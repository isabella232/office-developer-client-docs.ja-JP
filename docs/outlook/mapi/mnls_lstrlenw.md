---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392089"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="7df4d-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="7df4d-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="7df4d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7df4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7df4d-105">終端の null 文字を除く、指定した Unicode 文字列の長さを決定します。</span><span class="sxs-lookup"><span data-stu-id="7df4d-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="7df4d-106">[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)を代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="7df4d-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="7df4d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7df4d-107">Parameters</span></span>

 <span data-ttu-id="7df4d-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="7df4d-108">_lpsz_</span></span>
  
> <span data-ttu-id="7df4d-109">[in]チェックする null で終わる Unicode 文字列です。</span><span class="sxs-lookup"><span data-stu-id="7df4d-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7df4d-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="7df4d-110">Return value</span></span>

<span data-ttu-id="7df4d-111">関数は、文字列の長さの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="7df4d-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="7df4d-112">終端の null 文字を除いた文字列の文字数です。</span><span class="sxs-lookup"><span data-stu-id="7df4d-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="7df4d-113">_Lpsz_が NULL の場合は、関数は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="7df4d-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7df4d-114">備考</span><span class="sxs-lookup"><span data-stu-id="7df4d-114">Remarks</span></span>

<span data-ttu-id="7df4d-115">この関数は、**ライブラリ**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="7df4d-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="7df4d-116">詳細については、[ライブラリ](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df4d-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7df4d-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="7df4d-117">See also</span></span>



[<span data-ttu-id="7df4d-118">ライブラリ</span><span class="sxs-lookup"><span data-stu-id="7df4d-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="7df4d-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="7df4d-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

