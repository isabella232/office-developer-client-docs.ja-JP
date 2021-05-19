---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416266"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="1c02a-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="1c02a-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="1c02a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c02a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c02a-105">コンボ ボックス コントロールを記述するための [DTBLCOMBOBOX](dtblcombobox.md) 構造と、関連付けられた編集コントロールに入力できる最大文字数を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="1c02a-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c02a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1c02a-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c02a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c02a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1c02a-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="1c02a-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1c02a-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="1c02a-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="1c02a-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c02a-110">Parameters</span></span>

<span data-ttu-id="1c02a-111">_n_</span><span class="sxs-lookup"><span data-stu-id="1c02a-111">_n_</span></span>
  
> <span data-ttu-id="1c02a-112">コンボ ボックスの編集コントロールに入力できる文字数。</span><span class="sxs-lookup"><span data-stu-id="1c02a-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="1c02a-113">_u_</span><span class="sxs-lookup"><span data-stu-id="1c02a-113">_u_</span></span>
  
> <span data-ttu-id="1c02a-114">新しい構造の名前。</span><span class="sxs-lookup"><span data-stu-id="1c02a-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c02a-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1c02a-115">Remarks</span></span>

<span data-ttu-id="1c02a-116">**SizedDtblComboBox** マクロを使用すると、有効な文字列の長さが分かっているときにコンボ ボックスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="1c02a-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="1c02a-117">新しい構造は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="1c02a-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="1c02a-118">**SizedDtblComboBox** マクロから生成される構造体へのポインターを **DTBLCOMBOBOX** 構造体ポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="1c02a-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="1c02a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c02a-119">See also</span></span>

- [<span data-ttu-id="1c02a-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="1c02a-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="1c02a-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="1c02a-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

