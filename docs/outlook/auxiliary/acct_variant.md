---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント データ型のプロパティの値を保持します。
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799303"
---
# <a name="acctvariant"></a><span data-ttu-id="e8484-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="e8484-103">ACCT_VARIANT</span></span>

<span data-ttu-id="e8484-104">このデータ型の変数は、バリアント データ型のプロパティの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="e8484-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e8484-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e8484-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e8484-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="e8484-106">Members</span></span>

<span data-ttu-id="e8484-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="e8484-107">_dwType_</span></span>
  
> <span data-ttu-id="e8484-108">バリアントの種類です。</span><span class="sxs-lookup"><span data-stu-id="e8484-108">Type of variant:</span></span>
    
    - <span data-ttu-id="e8484-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e8484-109">PT_LONG</span></span>
    
    - <span data-ttu-id="e8484-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8484-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="e8484-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8484-111">PT_BINARY</span></span>
    
<span data-ttu-id="e8484-112">_dw_</span><span class="sxs-lookup"><span data-stu-id="e8484-112">_dw_</span></span>
  
> <span data-ttu-id="e8484-113">バリアントの DWORD 値です。</span><span class="sxs-lookup"><span data-stu-id="e8484-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="e8484-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="e8484-114">_pwsz_</span></span>
  
> <span data-ttu-id="e8484-115">バリアント型の値の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8484-115">String value of variant.</span></span>
    
<span data-ttu-id="e8484-116">_箱_</span><span class="sxs-lookup"><span data-stu-id="e8484-116">_bin_</span></span>
  
> <span data-ttu-id="e8484-117">バリアントのバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="e8484-117">Binary value of the variant.</span></span>
    

