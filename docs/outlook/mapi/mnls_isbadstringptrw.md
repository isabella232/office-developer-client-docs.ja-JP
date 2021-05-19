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
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356855"
---
# <a name="mnls_isbadstringptrw"></a><span data-ttu-id="1384b-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="1384b-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="1384b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1384b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1384b-105">ワイド文字列へのポインターが有効な値を確認します。</span><span class="sxs-lookup"><span data-stu-id="1384b-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="1384b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1384b-106">Parameters</span></span>

 <span data-ttu-id="1384b-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="1384b-107">_lpsz_</span></span>
  
> <span data-ttu-id="1384b-108">[in]ワイド文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1384b-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="1384b-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="1384b-109">_ucchMax_</span></span>
  
> <span data-ttu-id="1384b-110">[in]ターミネーターを含む文字の文字列の最大長。</span><span class="sxs-lookup"><span data-stu-id="1384b-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1384b-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="1384b-111">Return value</span></span>

<span data-ttu-id="1384b-112">文字列が正しい場合は true のブール型 (Boolean) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="1384b-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1384b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="1384b-113">Remarks</span></span>

<span data-ttu-id="1384b-114">この関数は [IsBadStringPtr をラップします](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1384b-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="1384b-115">詳細については [、「IsBadStringPtr」を参照してください](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1384b-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

