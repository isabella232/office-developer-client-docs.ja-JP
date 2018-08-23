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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593656"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="73121-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="73121-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="73121-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73121-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73121-105">コンボ ボックス コントロールと関連付けられたエディット コントロールに入力できる文字の最大数を記述するための[DTBLCOMBOBOX](dtblcombobox.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="73121-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73121-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="73121-106">Header file:</span></span>  <br/> |<span data-ttu-id="73121-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73121-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="73121-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="73121-108">Related structure:</span></span>  <br/> |<span data-ttu-id="73121-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="73121-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="73121-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73121-110">Parameters</span></span>

<span data-ttu-id="73121-111">_n_</span><span class="sxs-lookup"><span data-stu-id="73121-111">_n_</span></span>
  
> <span data-ttu-id="73121-112">コンボ ボックスの入力できる文字数は、コントロールを編集します。</span><span class="sxs-lookup"><span data-stu-id="73121-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="73121-113">_u_</span><span class="sxs-lookup"><span data-stu-id="73121-113">_u_</span></span>
  
> <span data-ttu-id="73121-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="73121-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73121-115">注釈</span><span class="sxs-lookup"><span data-stu-id="73121-115">Remarks</span></span>

<span data-ttu-id="73121-116">**SizedDtblComboBox**マクロを使用して、有効な文字の文字列の長さがわかっている場合は、コンボ ボックスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="73121-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="73121-117">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="73121-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="73121-118">**DTBLCOMBOBOX**構造体のポインターとして、 **SizedDtblComboBox**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="73121-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="73121-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="73121-119">See also</span></span>

- [<span data-ttu-id="73121-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="73121-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="73121-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="73121-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

