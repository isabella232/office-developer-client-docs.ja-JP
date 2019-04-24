---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: '最終更新日: 2012 年6月18日'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341728"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="f9c30-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="f9c30-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="f9c30-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9c30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9c30-105">文字列をバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f9c30-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="f9c30-106">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f9c30-106">Do not use.</span></span> <span data-ttu-id="f9c30-107">代わりに、 [stringcchcopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx)を使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="f9c30-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="f9c30-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9c30-108">Parameters</span></span>

<span data-ttu-id="f9c30-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="f9c30-109">lpString1</span></span>
  
> <span data-ttu-id="f9c30-110">読み上げlpString2 パラメーターによって示される文字列の内容を受信するバッファー。</span><span class="sxs-lookup"><span data-stu-id="f9c30-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="f9c30-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="f9c30-111">lpString2</span></span>
  
> <span data-ttu-id="f9c30-112">順番コピーする null で終わる文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9c30-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9c30-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9c30-113">Return value</span></span>

<span data-ttu-id="f9c30-114">関数が正常に終了した場合、戻り値はバッファーへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="f9c30-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="f9c30-115">関数が失敗した場合、戻り値は null で、lpString1 を null で終了することはできません。</span><span class="sxs-lookup"><span data-stu-id="f9c30-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9c30-116">解説</span><span class="sxs-lookup"><span data-stu-id="f9c30-116">Remarks</span></span>

<span data-ttu-id="f9c30-117">この関数は、 **lstrcpy**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="f9c30-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="f9c30-118">詳細については、「 [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9c30-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9c30-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9c30-119">See also</span></span>



[<span data-ttu-id="f9c30-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="f9c30-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

