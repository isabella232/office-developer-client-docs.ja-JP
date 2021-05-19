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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341728"
---
# <a name="mnls_lstrcpyw"></a><span data-ttu-id="54551-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="54551-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="54551-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54551-105">文字列をバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="54551-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="54551-106">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="54551-106">Do not use.</span></span> <span data-ttu-id="54551-107">代わりに [StringCchCopy の使用](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) を検討してください。</span><span class="sxs-lookup"><span data-stu-id="54551-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="54551-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="54551-108">Parameters</span></span>

<span data-ttu-id="54551-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="54551-109">lpString1</span></span>
  
> <span data-ttu-id="54551-110">[out]lpString2 パラメーターが指す文字列の内容を受け取るバッファー。</span><span class="sxs-lookup"><span data-stu-id="54551-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="54551-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="54551-111">lpString2</span></span>
  
> <span data-ttu-id="54551-112">[in]コピーする null 終端文字列。</span><span class="sxs-lookup"><span data-stu-id="54551-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54551-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="54551-113">Return value</span></span>

<span data-ttu-id="54551-114">関数が成功した場合、戻り値はバッファーへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="54551-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="54551-115">関数が失敗した場合、戻り値は NULL で、lpString1 は null 終了しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54551-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54551-116">注釈</span><span class="sxs-lookup"><span data-stu-id="54551-116">Remarks</span></span>

<span data-ttu-id="54551-117">この関数は **、lstrcpy 関数をラップ** します。</span><span class="sxs-lookup"><span data-stu-id="54551-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="54551-118">詳細については [、「lstrcpy」を参照してください](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="54551-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54551-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="54551-119">See also</span></span>



[<span data-ttu-id="54551-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="54551-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

