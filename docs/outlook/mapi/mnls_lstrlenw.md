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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801674"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="608aa-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="608aa-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="608aa-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="608aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="608aa-105">終端の null 文字を除く、指定した Unicode 文字列の長さを決定します。</span><span class="sxs-lookup"><span data-stu-id="608aa-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="608aa-106">[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)を代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="608aa-106">Consider using [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="608aa-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="608aa-107">Parameters</span></span>

 <span data-ttu-id="608aa-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="608aa-108">_lpsz_</span></span>
  
> <span data-ttu-id="608aa-109">[in]チェックする null で終わる Unicode 文字列です。</span><span class="sxs-lookup"><span data-stu-id="608aa-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="608aa-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="608aa-110">Return value</span></span>

<span data-ttu-id="608aa-111">関数は、文字列の長さの整数を返します。</span><span class="sxs-lookup"><span data-stu-id="608aa-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="608aa-112">終端の null 文字を除いた文字列の文字数です。</span><span class="sxs-lookup"><span data-stu-id="608aa-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="608aa-113">_Lpsz_が NULL の場合は、関数は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="608aa-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="608aa-114">備考</span><span class="sxs-lookup"><span data-stu-id="608aa-114">Remarks</span></span>

<span data-ttu-id="608aa-115">この関数は、**ライブラリ**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="608aa-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="608aa-116">詳細については、[ライブラリ](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="608aa-116">For more information, see [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="608aa-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="608aa-117">See also</span></span>



[<span data-ttu-id="608aa-118">ライブラリ</span><span class="sxs-lookup"><span data-stu-id="608aa-118">lstrlen</span></span>](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="608aa-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="608aa-119">StringCchLength</span></span>](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

