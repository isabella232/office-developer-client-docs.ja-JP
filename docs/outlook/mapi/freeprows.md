---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328015"
---
# <a name="freeprows"></a><span data-ttu-id="f4aef-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="f4aef-103">FreeProws</span></span>

  
  
<span data-ttu-id="f4aef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4aef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4aef-105">[srowset](srowset.md)構造を破棄し、すべてのメンバー配列および構造体に割り当てられたメモリを含む、関連するメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="f4aef-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4aef-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f4aef-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4aef-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="f4aef-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f4aef-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f4aef-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4aef-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4aef-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4aef-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f4aef-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4aef-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="f4aef-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="f4aef-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4aef-112">Parameters</span></span>

 <span data-ttu-id="f4aef-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="f4aef-113">_prows_</span></span>
  
> <span data-ttu-id="f4aef-114">順番破棄する**srowset**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4aef-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f4aef-115">Return value</span><span class="sxs-lookup"><span data-stu-id="f4aef-115">Return value</span></span>

<span data-ttu-id="f4aef-116">なし。</span><span class="sxs-lookup"><span data-stu-id="f4aef-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4aef-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f4aef-117">Notes to callers</span></span>

<span data-ttu-id="f4aef-118">MAPI の実装の一部と\*\*\*\* して、MAPI は[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、完全な構造を解放する前に、 **srowset**構造のすべてのエントリを解放します。</span><span class="sxs-lookup"><span data-stu-id="f4aef-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="f4aef-119">そのため、このようなすべてのエントリは、各メンバーの配列および構造に対して個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して、 [srowset](srowset.md)構造の割り当てルールに従っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4aef-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="f4aef-120">**adrlist**および**srowset**構造体のメモリ割り当ての詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4aef-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4aef-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f4aef-121">MFCMAPI reference</span></span>

<span data-ttu-id="f4aef-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4aef-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4aef-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f4aef-123">**File**</span></span>|<span data-ttu-id="f4aef-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="f4aef-124">**Function**</span></span>|<span data-ttu-id="f4aef-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f4aef-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4aef-126">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="f4aef-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f4aef-127">dwthreadの loadtable</span><span class="sxs-lookup"><span data-stu-id="f4aef-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="f4aef-128">mfcmapi は、 **freeprows**メソッドを使用して、処理されているテーブルの行を含む srowset 構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="f4aef-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4aef-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4aef-129">See also</span></span>



<span data-ttu-id="f4aef-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f4aef-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

