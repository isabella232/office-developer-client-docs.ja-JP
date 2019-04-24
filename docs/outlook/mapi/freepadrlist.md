---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328036"
---
# <a name="freepadrlist"></a><span data-ttu-id="dc8b8-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="dc8b8-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="dc8b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc8b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc8b8-105">[adrlist](adrlist.md)構造体を破棄し、すべてのメンバー配列および構造体に割り当てられたメモリを含む、関連するメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc8b8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc8b8-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="dc8b8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dc8b8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc8b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc8b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc8b8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc8b8-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="dc8b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="dc8b8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dc8b8-112">Parameters</span></span>

 <span data-ttu-id="dc8b8-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="dc8b8-113">_padrlist_</span></span>
  
> <span data-ttu-id="dc8b8-114">順番破棄する**adrlist**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc8b8-115">Return value</span><span class="sxs-lookup"><span data-stu-id="dc8b8-115">Return value</span></span>

<span data-ttu-id="dc8b8-116">なし。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc8b8-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dc8b8-117">Notes to callers</span></span>

<span data-ttu-id="dc8b8-118">[MAPIFreeBuffer](mapifreebuffer.md)関数は、 **freepadrlist**の実装の一環として、完全な構造を解放する前に**adrlist**構造体のすべてのエントリを解放するために呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="dc8b8-119">そのため、このようなエントリはすべて、各メンバーの配列および構造に対して個別の[MAPIAllocateBuffer](mapiallocatebuffer.md)呼び出しを使用して、 [adrlist](adrlist.md)構造の割り当てルールに従っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="dc8b8-120">**adrlist**および**srowset**構造体のメモリ割り当ての詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc8b8-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="dc8b8-121">MFCMAPI reference</span></span>

<span data-ttu-id="dc8b8-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc8b8-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-123">**File**</span></span>|<span data-ttu-id="dc8b8-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-124">**Function**</span></span>|<span data-ttu-id="dc8b8-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc8b8-126">MAPIABFunctions</span><span class="sxs-lookup"><span data-stu-id="dc8b8-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="dc8b8-127">addoneoffaddress</span><span class="sxs-lookup"><span data-stu-id="dc8b8-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="dc8b8-128">mfcmapi は、 **freepadrlist**メソッドを使用して、メッセージに1回限りのアドレスを追加するために構築された adrlist 構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="dc8b8-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc8b8-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="dc8b8-129">See also</span></span>



<span data-ttu-id="dc8b8-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

