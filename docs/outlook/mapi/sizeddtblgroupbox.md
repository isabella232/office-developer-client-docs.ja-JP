---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419318"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="55ef6-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="55ef6-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="55ef6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55ef6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55ef6-105">グループボックスコントロールと指定された長さのラベルを表す[dtblgroupbox](dtblgroupbox.md)構造を含む名前付き構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="55ef6-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55ef6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="55ef6-106">Header file:</span></span>  <br/> |<span data-ttu-id="55ef6-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55ef6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="55ef6-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="55ef6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="55ef6-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="55ef6-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="55ef6-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="55ef6-110">Parameters</span></span>

<span data-ttu-id="55ef6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="55ef6-111">_n_</span></span>
  
> <span data-ttu-id="55ef6-112">グループボックスのラベルの長さ。</span><span class="sxs-lookup"><span data-stu-id="55ef6-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="55ef6-113">_u_</span><span class="sxs-lookup"><span data-stu-id="55ef6-113">_u_</span></span>
  
> <span data-ttu-id="55ef6-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="55ef6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55ef6-115">注釈</span><span class="sxs-lookup"><span data-stu-id="55ef6-115">Remarks</span></span>

<span data-ttu-id="55ef6-116">**sizeddtblgroupbox**マクロを使用すると、ラベルの長さが既知の場合に、グループボックスコントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="55ef6-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="55ef6-117">次のメンバーで新しい構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="55ef6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="55ef6-118">**sizeddtblgroupbox**マクロの結果として得られる構造体へのポインターを**dtblgroupbox**構造のポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="55ef6-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="55ef6-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="55ef6-119">See also</span></span>

- [<span data-ttu-id="55ef6-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="55ef6-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="55ef6-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="55ef6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

