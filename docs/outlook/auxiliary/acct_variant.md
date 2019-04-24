---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント型 (variant) のデータ型のプロパティの値を保持します。
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316920"
---
# <a name="acctvariant"></a><span data-ttu-id="e5ab0-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="e5ab0-103">ACCT_VARIANT</span></span>

<span data-ttu-id="e5ab0-104">このデータ型の変数は、バリアント型 (variant) のデータ型のプロパティの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="e5ab0-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5ab0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e5ab0-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e5ab0-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="e5ab0-106">Members</span></span>

<span data-ttu-id="e5ab0-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="e5ab0-107">_dwType_</span></span>
  
> <span data-ttu-id="e5ab0-108">バリアントの種類:</span><span class="sxs-lookup"><span data-stu-id="e5ab0-108">Type of variant:</span></span>
    
    - <span data-ttu-id="e5ab0-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e5ab0-109">PT_LONG</span></span>
    
    - <span data-ttu-id="e5ab0-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5ab0-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="e5ab0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e5ab0-111">PT_BINARY</span></span>
    
<span data-ttu-id="e5ab0-112">_dw_</span><span class="sxs-lookup"><span data-stu-id="e5ab0-112">_dw_</span></span>
  
> <span data-ttu-id="e5ab0-113">variant の DWORD 値。</span><span class="sxs-lookup"><span data-stu-id="e5ab0-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="e5ab0-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="e5ab0-114">_pwsz_</span></span>
  
> <span data-ttu-id="e5ab0-115">variant の文字列値。</span><span class="sxs-lookup"><span data-stu-id="e5ab0-115">String value of variant.</span></span>
    
<span data-ttu-id="e5ab0-116">_在庫_</span><span class="sxs-lookup"><span data-stu-id="e5ab0-116">_bin_</span></span>
  
> <span data-ttu-id="e5ab0-117">バリアント型 (variant) のバイナリ値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5ab0-117">Binary value of the variant.</span></span>
    

