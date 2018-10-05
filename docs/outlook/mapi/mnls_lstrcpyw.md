---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: '最終更新日: 2012 年 6 月 18 日'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382709"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="7c574-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="7c574-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="7c574-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c574-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c574-105">文字列をバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7c574-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="7c574-106">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7c574-106">Do not use.</span></span> <span data-ttu-id="7c574-107">[StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="7c574-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="7c574-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c574-108">Parameters</span></span>

<span data-ttu-id="7c574-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="7c574-109">lpString1</span></span>
  
> <span data-ttu-id="7c574-110">[out]LpString2 パラメーターが指す文字列の内容を受信するバッファーです。</span><span class="sxs-lookup"><span data-stu-id="7c574-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="7c574-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="7c574-111">lpString2</span></span>
  
> <span data-ttu-id="7c574-112">[in]Null で終わる文字列をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7c574-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c574-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="7c574-113">Return value</span></span>

<span data-ttu-id="7c574-114">関数が成功した場合は、バッファーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="7c574-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="7c574-115">関数が失敗した場合、NULL が戻り値と lpString1 できない場合があります null で終わる。</span><span class="sxs-lookup"><span data-stu-id="7c574-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c574-116">備考</span><span class="sxs-lookup"><span data-stu-id="7c574-116">Remarks</span></span>

<span data-ttu-id="7c574-117">この関数は、 **lstrcpy**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="7c574-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="7c574-118">詳細については、 [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c574-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c574-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c574-119">See also</span></span>



[<span data-ttu-id="7c574-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="7c574-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

