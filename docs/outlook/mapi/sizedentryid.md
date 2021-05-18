---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405710"
---
# <a name="sizedentryid"></a><span data-ttu-id="7a69b-103">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a69b-103">SizedENTRYID</span></span>

<span data-ttu-id="7a69b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a69b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a69b-105">指定したサイズの [ab メンバー](entryid.md) を含む名前付き **ENTRYID** 構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a69b-105">Creates a named [ENTRYID](entryid.md) structure that contains an **ab** member of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a69b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7a69b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a69b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a69b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a69b-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="7a69b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7a69b-109">**ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="7a69b-109">**ENTRYID**</span></span> <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a><span data-ttu-id="7a69b-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a69b-110">Parameters</span></span>

<span data-ttu-id="7a69b-111">_ _cb_</span><span class="sxs-lookup"><span data-stu-id="7a69b-111">_ _cb_</span></span>
  
> <span data-ttu-id="7a69b-112">新しい構造体の **ab メンバー** のバイト数。</span><span class="sxs-lookup"><span data-stu-id="7a69b-112">Count of bytes in the **ab** member of the new structure.</span></span> 
    
<span data-ttu-id="7a69b-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="7a69b-113">_ _name_</span></span>
  
> <span data-ttu-id="7a69b-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="7a69b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a69b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7a69b-115">Remarks</span></span>

<span data-ttu-id="7a69b-116">**SizedENTRYID** マクロを使用すると、配列の長さの要件が分かった後にエントリ識別子を定義できます。</span><span class="sxs-lookup"><span data-stu-id="7a69b-116">The **SizedENTRYID** macro lets you define an entry identifier after array length requirements are known.</span></span> <span data-ttu-id="7a69b-117">明示的な境界を持つエントリ識別子を作成するには、このマクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a69b-117">Use this macro to create an entry identifier with explicit bounds.</span></span> 
  
<span data-ttu-id="7a69b-118">**SizedENTRYID** マクロの結果として新しい構造を **ENTRYID** 構造体へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7a69b-118">To use the new structure that results from the **SizedENTRYID** macro as a pointer to an **ENTRYID** structure, perform the following cast:</span></span> 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a><span data-ttu-id="7a69b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a69b-119">See also</span></span>

- [<span data-ttu-id="7a69b-120">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a69b-120">ENTRYID</span></span>](entryid.md)
- [<span data-ttu-id="7a69b-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="7a69b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

