---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803923"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="5b6cd-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="5b6cd-103">SizedDtblPage</span></span>

<span data-ttu-id="5b6cd-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b6cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b6cd-105">タブ付きページのコントロール、指定した長さのラベル、ヘルプ ファイルのエントリを指定された長さの記述するため[DTBLPAGE](dtblpage.md)構造体を含む名前付き構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b6cd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5b6cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5b6cd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b6cd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5b6cd-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5b6cd-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="5b6cd-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="5b6cd-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b6cd-110">Parameters</span></span>

<span data-ttu-id="5b6cd-111">_n_</span><span class="sxs-lookup"><span data-stu-id="5b6cd-111">_n_</span></span>
  
> <span data-ttu-id="5b6cd-112">[ページ] タブのラベルの長さです。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="5b6cd-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="5b6cd-113">_n1_</span></span>
  
> <span data-ttu-id="5b6cd-114">タブ ページ コントロールを使用するヘルプ ファイルを識別する、Mapisvc.inf ファイルに表示されるエントリの長さです。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="5b6cd-115">_u_</span><span class="sxs-lookup"><span data-stu-id="5b6cd-115">_u_</span></span>
  
> <span data-ttu-id="5b6cd-116">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b6cd-117">注釈</span><span class="sxs-lookup"><span data-stu-id="5b6cd-117">Remarks</span></span>

<span data-ttu-id="5b6cd-118">**SizedDtblPage**マクロを使用して、ヘルプ ファイルのエントリと関連付けられているラベルの文字数がわかっている場合は、タブ付きページのコントロールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="5b6cd-119">新しい構造体は、次のメンバーで作成されます。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="5b6cd-120">**DTBLPAGE**構造体のポインターとして、 **SizedDtblPage**マクロからの結果の構造にポインターを使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="5b6cd-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="5b6cd-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b6cd-121">See also</span></span>

- [<span data-ttu-id="5b6cd-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5b6cd-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="5b6cd-123">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="5b6cd-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

