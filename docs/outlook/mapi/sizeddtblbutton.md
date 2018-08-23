---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590345"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="bb749-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="bb749-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="bb749-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb749-105">ボタンと指定された長さのラベルを記述するための[DTBLBUTTON](dtblbutton.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="bb749-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb749-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bb749-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb749-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb749-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bb749-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="bb749-108">Related structure:</span></span>  <br/> |<span data-ttu-id="bb749-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="bb749-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="bb749-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb749-110">Parameters</span></span>

 <span data-ttu-id="bb749-111">_n_</span><span class="sxs-lookup"><span data-stu-id="bb749-111">_n_</span></span>
  
> <span data-ttu-id="bb749-112">新しい構造体に含まれるラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="bb749-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="bb749-113">_u_</span><span class="sxs-lookup"><span data-stu-id="bb749-113">_u_</span></span>
  
> <span data-ttu-id="bb749-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="bb749-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb749-115">注釈</span><span class="sxs-lookup"><span data-stu-id="bb749-115">Remarks</span></span>

<span data-ttu-id="bb749-116">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="bb749-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="bb749-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb749-117">See also</span></span>



[<span data-ttu-id="bb749-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="bb749-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="bb749-119">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="bb749-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

