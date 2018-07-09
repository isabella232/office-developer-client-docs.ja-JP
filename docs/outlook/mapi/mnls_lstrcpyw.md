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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801657"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="0a349-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="0a349-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="0a349-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a349-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a349-105">文字列をバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0a349-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="0a349-106">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0a349-106">Do not use.</span></span> <span data-ttu-id="0a349-107">[StringCchCopy](http://msdn.microsoft.com/ja-jp/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。</span><span class="sxs-lookup"><span data-stu-id="0a349-107">Consider using [StringCchCopy](http://msdn.microsoft.com/ja-jp/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="0a349-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="0a349-108">Parameters</span></span>

<span data-ttu-id="0a349-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="0a349-109">lpString1</span></span>
  
> <span data-ttu-id="0a349-110">[out]LpString2 パラメーターが指す文字列の内容を受信するバッファーです。</span><span class="sxs-lookup"><span data-stu-id="0a349-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="0a349-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="0a349-111">lpString2</span></span>
  
> <span data-ttu-id="0a349-112">[in]Null で終わる文字列をコピーします。</span><span class="sxs-lookup"><span data-stu-id="0a349-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a349-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0a349-113">Return value</span></span>

<span data-ttu-id="0a349-114">関数が成功した場合は、バッファーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="0a349-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="0a349-115">関数が失敗した場合、NULL が戻り値と lpString1 できない場合があります null で終わる。</span><span class="sxs-lookup"><span data-stu-id="0a349-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a349-116">備考</span><span class="sxs-lookup"><span data-stu-id="0a349-116">Remarks</span></span>

<span data-ttu-id="0a349-117">この関数は、 **lstrcpy**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="0a349-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="0a349-118">詳細については、 [lstrcpy](http://msdn.microsoft.com/ja-jp/library/ms647490%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a349-118">For more information, see [lstrcpy](http://msdn.microsoft.com/ja-jp/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a349-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a349-119">See also</span></span>



[<span data-ttu-id="0a349-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="0a349-120">lstrcpy</span></span>](http://msdn.microsoft.com/ja-jp/library/ms647490%28VS.85%29.aspx)

