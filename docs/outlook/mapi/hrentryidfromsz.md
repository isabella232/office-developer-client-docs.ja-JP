---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800297"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="fe1cb-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="fe1cb-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="fe1cb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe1cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe1cb-105">ASCII エンコードからエントリ識別子を再作成します。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe1cb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fe1cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe1cb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fe1cb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fe1cb-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe1cb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe1cb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fe1cb-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-110">Called by:</span></span>  <br/> |<span data-ttu-id="fe1cb-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="fe1cb-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="fe1cb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe1cb-112">Parameters</span></span>

 <span data-ttu-id="fe1cb-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="fe1cb-113">_sz_</span></span>
  
> <span data-ttu-id="fe1cb-114">[in]エントリ識別子を作成するから ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="fe1cb-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="fe1cb-115">_pcb_</span></span>
  
> <span data-ttu-id="fe1cb-116">[out]_Ppentry_パラメーターで指定されたエントリの識別子のバイト単位のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="fe1cb-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="fe1cb-117">_ppentry_</span></span>
  
> <span data-ttu-id="fe1cb-118">[out]新しいエントリの識別子を格納する返される[エントリ ID](entryid.md)の構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe1cb-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fe1cb-119">Return value</span></span>

<span data-ttu-id="fe1cb-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe1cb-120">S_OK</span></span>
  
> <span data-ttu-id="fe1cb-121">再作成に成功しました。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-121">The recreation was successful.</span></span>
    
<span data-ttu-id="fe1cb-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fe1cb-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="fe1cb-123">エントリ ID が無効でした。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe1cb-124">備考</span><span class="sxs-lookup"><span data-stu-id="fe1cb-124">Remarks</span></span>

<span data-ttu-id="fe1cb-125">**HrEntryIDFromSz**と[HrSzFromEntryID](hrszfromentryid.md)関数は、文字列とエントリの識別子のバイナリ フォーマット間の変換を提供します。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fe1cb-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fe1cb-126">Notes to callers</span></span>

<span data-ttu-id="fe1cb-127">**HrEntryIDFromSz**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fe1cb-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

