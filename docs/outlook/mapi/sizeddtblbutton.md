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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421915"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="1ab78-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="1ab78-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="1ab78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ab78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ab78-105">ボタンと指定した長さのラベルを記述するための [DTBLBUTTON](dtblbutton.md) 構造を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="1ab78-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ab78-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1ab78-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ab78-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ab78-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1ab78-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="1ab78-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1ab78-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="1ab78-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="1ab78-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ab78-110">Parameters</span></span>

 <span data-ttu-id="1ab78-111">_n_</span><span class="sxs-lookup"><span data-stu-id="1ab78-111">_n_</span></span>
  
> <span data-ttu-id="1ab78-112">新しい構造に含めるラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="1ab78-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="1ab78-113">_u_</span><span class="sxs-lookup"><span data-stu-id="1ab78-113">_u_</span></span>
  
> <span data-ttu-id="1ab78-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="1ab78-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ab78-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1ab78-115">Remarks</span></span>

<span data-ttu-id="1ab78-116">新しい構造は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="1ab78-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="1ab78-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ab78-117">See also</span></span>



[<span data-ttu-id="1ab78-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="1ab78-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="1ab78-119">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="1ab78-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

