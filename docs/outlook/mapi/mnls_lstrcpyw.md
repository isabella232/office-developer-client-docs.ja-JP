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
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575463"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="9814d-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="9814d-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="9814d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9814d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9814d-105">文字列をバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9814d-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="9814d-106">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9814d-106">Do not use.</span></span> <span data-ttu-id="9814d-107">[StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="9814d-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="9814d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9814d-108">Parameters</span></span>

<span data-ttu-id="9814d-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="9814d-109">lpString1</span></span>
  
> <span data-ttu-id="9814d-110">[out]LpString2 パラメーターが指す文字列の内容を受信するバッファーです。</span><span class="sxs-lookup"><span data-stu-id="9814d-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="9814d-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="9814d-111">lpString2</span></span>
  
> <span data-ttu-id="9814d-112">[in]Null で終わる文字列をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9814d-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9814d-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="9814d-113">Return value</span></span>

<span data-ttu-id="9814d-114">関数が成功した場合は、バッファーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9814d-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="9814d-115">関数が失敗した場合、NULL が戻り値と lpString1 できない場合があります null で終わる。</span><span class="sxs-lookup"><span data-stu-id="9814d-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9814d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="9814d-116">Remarks</span></span>

<span data-ttu-id="9814d-117">この関数は、 **lstrcpy**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="9814d-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="9814d-118">詳細については、 [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9814d-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9814d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="9814d-119">See also</span></span>



[<span data-ttu-id="9814d-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="9814d-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

