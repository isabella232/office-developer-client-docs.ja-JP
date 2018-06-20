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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800132"
---
# <a name="freepadrlist"></a><span data-ttu-id="e7e25-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="e7e25-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="e7e25-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7e25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7e25-105">[ADRLIST](adrlist.md)構造体を破棄し、すべてのアレイ メンバーと構造体に割り当てられたメモリを含む、関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="e7e25-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7e25-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e7e25-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7e25-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7e25-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7e25-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e7e25-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7e25-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7e25-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7e25-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e7e25-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7e25-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7e25-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="e7e25-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e7e25-112">Parameters</span></span>

 <span data-ttu-id="e7e25-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="e7e25-113">_padrlist_</span></span>
  
> <span data-ttu-id="e7e25-114">[in]破棄する**ADRLIST**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e7e25-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7e25-115">Return value</span><span class="sxs-lookup"><span data-stu-id="e7e25-115">Return value</span></span>

<span data-ttu-id="e7e25-116">なし。</span><span class="sxs-lookup"><span data-stu-id="e7e25-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7e25-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e7e25-117">Notes to callers</span></span>

<span data-ttu-id="e7e25-118">**FreePadrlist**の実装の一部としては、MAPI は、完全な構造を解放する前に**ADRLIST**構造体のすべてのエントリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7e25-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="e7e25-119">このためこのようなすべてのエントリは[ADRLIST](adrlist.md)構造体の割り当て規則に従っている必要があります、個人を使用して[MAPIAllocateBuffer](mapiallocatebuffer.md)を各メンバーの配列と構造体を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7e25-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="e7e25-120">**ADRLIST**と**SRowSet**構造体のメモリの割り当ての詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7e25-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e7e25-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="e7e25-121">MFCMAPI reference</span></span>

<span data-ttu-id="e7e25-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e7e25-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e7e25-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="e7e25-123">**File**</span></span>|<span data-ttu-id="e7e25-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="e7e25-124">**Function**</span></span>|<span data-ttu-id="e7e25-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="e7e25-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e7e25-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e7e25-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e7e25-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="e7e25-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="e7e25-128">MFCMAPI では、 **FreePadrlist**メソッドを使用して、1 回限りのアドレスをメッセージに追加するのには構築された ADRLIST 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="e7e25-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7e25-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7e25-129">See also</span></span>



<span data-ttu-id="e7e25-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e7e25-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

