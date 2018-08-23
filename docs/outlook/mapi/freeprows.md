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
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800125"
---
# <a name="freeprows"></a><span data-ttu-id="f7adb-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="f7adb-103">FreeProws</span></span>

  
  
<span data-ttu-id="f7adb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7adb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7adb-105">[SRowSet](srowset.md)構造体を破棄し、すべてのアレイ メンバーと構造体に割り当てられたメモリを含む、関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="f7adb-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7adb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f7adb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7adb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f7adb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f7adb-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f7adb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7adb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7adb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7adb-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f7adb-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7adb-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f7adb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="f7adb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7adb-112">Parameters</span></span>

 <span data-ttu-id="f7adb-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="f7adb-113">_prows_</span></span>
  
> <span data-ttu-id="f7adb-114">[in]破棄する**SRowSet**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7adb-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7adb-115">Return value</span><span class="sxs-lookup"><span data-stu-id="f7adb-115">Return value</span></span>

<span data-ttu-id="f7adb-116">なし。</span><span class="sxs-lookup"><span data-stu-id="f7adb-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f7adb-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f7adb-117">Notes to callers</span></span>

<span data-ttu-id="f7adb-118">**FreeProws**の実装の一部としては、MAPI は、完全な構造を解放する前に**SRowSet**構造内のすべてのエントリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f7adb-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="f7adb-119">このためこのようなすべてのエントリは[SRowSet](srowset.md)構造体の割り当て規則に従っている必要があります、個人を使用して[MAPIAllocateBuffer](mapiallocatebuffer.md)を各メンバーの配列と構造体を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f7adb-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="f7adb-120">**ADRLIST**と**SRowSet**構造体のメモリの割り当ての詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7adb-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7adb-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f7adb-121">MFCMAPI reference</span></span>

<span data-ttu-id="f7adb-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f7adb-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7adb-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f7adb-123">**File**</span></span>|<span data-ttu-id="f7adb-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f7adb-124">**Function**</span></span>|<span data-ttu-id="f7adb-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f7adb-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7adb-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f7adb-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f7adb-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="f7adb-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="f7adb-128">MFCMAPI では、 **FreeProws**メソッドを使用して、処理するテーブルの行を含む、SRowSet 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="f7adb-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7adb-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7adb-129">See also</span></span>



<span data-ttu-id="f7adb-130">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f7adb-130">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

