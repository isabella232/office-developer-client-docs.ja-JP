---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282755"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="ce6ff-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="ce6ff-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="ce6ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce6ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce6ff-105">チェックボックスコントロールと指定された長さのラベルを記述するための[dtblcheckbox](dtblcheckbox.md)構造を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce6ff-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce6ff-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce6ff-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ce6ff-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="ce6ff-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ce6ff-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="ce6ff-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="ce6ff-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ce6ff-110">Parameters</span></span>

<span data-ttu-id="ce6ff-111">_n_</span><span class="sxs-lookup"><span data-stu-id="ce6ff-111">_n_</span></span>
  
> <span data-ttu-id="ce6ff-112">新しい構造に含めるラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="ce6ff-113">_u_</span><span class="sxs-lookup"><span data-stu-id="ce6ff-113">_u_</span></span>
  
> <span data-ttu-id="ce6ff-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce6ff-115">解説</span><span class="sxs-lookup"><span data-stu-id="ce6ff-115">Remarks</span></span>

<span data-ttu-id="ce6ff-116">**sizeddtblcheckbox**マクロを使用すると、ラベル文字の数が既知の場合にチェックボックスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="ce6ff-117">次のメンバーで新しい構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="ce6ff-118">**sizeddtblcheckbox**マクロの結果として得られる構造体へのポインターを**dtblcheckbox**構造体ポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="ce6ff-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="ce6ff-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce6ff-119">See also</span></span>

- [<span data-ttu-id="ce6ff-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="ce6ff-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="ce6ff-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="ce6ff-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

