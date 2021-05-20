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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437729"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="5ae46-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="5ae46-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="5ae46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ae46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ae46-105">ASCII エンコードからエントリ識別子を再作成します。</span><span class="sxs-lookup"><span data-stu-id="5ae46-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ae46-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5ae46-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ae46-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5ae46-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5ae46-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5ae46-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5ae46-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5ae46-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5ae46-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5ae46-110">Called by:</span></span>  <br/> |<span data-ttu-id="5ae46-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5ae46-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="5ae46-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ae46-112">Parameters</span></span>

 <span data-ttu-id="5ae46-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="5ae46-113">_sz_</span></span>
  
> <span data-ttu-id="5ae46-114">[in]エントリ識別子を作成する ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ae46-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="5ae46-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="5ae46-115">_pcb_</span></span>
  
> <span data-ttu-id="5ae46-116">[out]  _ppentry_ パラメーターが指すエントリ識別子のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ae46-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="5ae46-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="5ae46-117">_ppentry_</span></span>
  
> <span data-ttu-id="5ae46-118">[out]新しいエントリ識別子を含む、返 [される ENTRYID](entryid.md) 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ae46-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5ae46-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="5ae46-119">Return value</span></span>

<span data-ttu-id="5ae46-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ae46-120">S_OK</span></span>
  
> <span data-ttu-id="5ae46-121">レクリエーションは成功しました。</span><span class="sxs-lookup"><span data-stu-id="5ae46-121">The recreation was successful.</span></span>
    
<span data-ttu-id="5ae46-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5ae46-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="5ae46-123">エントリ ID が無効でした。</span><span class="sxs-lookup"><span data-stu-id="5ae46-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ae46-124">注釈</span><span class="sxs-lookup"><span data-stu-id="5ae46-124">Remarks</span></span>

<span data-ttu-id="5ae46-125">**HrEntryIDFromSz** 関数と [HrSzFromEntryID](hrszfromentryid.md)関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ae46-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ae46-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5ae46-126">Notes to callers</span></span>

<span data-ttu-id="5ae46-127">**HrEntryIDFromSz** 関数は [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5ae46-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

