---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント 型であるプロパティの値を保持します。
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424400"
---
# <a name="acct_variant"></a><span data-ttu-id="b7c11-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="b7c11-103">ACCT_VARIANT</span></span>

<span data-ttu-id="b7c11-104">このデータ型の変数は、バリアント 型であるプロパティの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="b7c11-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b7c11-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b7c11-105">Quick info</span></span>

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a><span data-ttu-id="b7c11-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="b7c11-106">Members</span></span>

<span data-ttu-id="b7c11-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="b7c11-107">_dwType_</span></span>
  
> <span data-ttu-id="b7c11-108">バリアントの種類:</span><span class="sxs-lookup"><span data-stu-id="b7c11-108">Type of variant:</span></span>
    
    - <span data-ttu-id="b7c11-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b7c11-109">PT_LONG</span></span>
    
    - <span data-ttu-id="b7c11-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7c11-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="b7c11-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7c11-111">PT_BINARY</span></span>
    
<span data-ttu-id="b7c11-112">_dw_</span><span class="sxs-lookup"><span data-stu-id="b7c11-112">_dw_</span></span>
  
> <span data-ttu-id="b7c11-113">バリアントの DWORD 値。</span><span class="sxs-lookup"><span data-stu-id="b7c11-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="b7c11-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="b7c11-114">_pwsz_</span></span>
  
> <span data-ttu-id="b7c11-115">variant の文字列値。</span><span class="sxs-lookup"><span data-stu-id="b7c11-115">String value of variant.</span></span>
    
<span data-ttu-id="b7c11-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="b7c11-116">_bin_</span></span>
  
> <span data-ttu-id="b7c11-117">バリアントのバイナリ値。</span><span class="sxs-lookup"><span data-stu-id="b7c11-117">Binary value of the variant.</span></span>
    

