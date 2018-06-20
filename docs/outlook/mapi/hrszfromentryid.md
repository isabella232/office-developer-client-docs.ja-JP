---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800314"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="2cfbf-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="2cfbf-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="2cfbf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cfbf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cfbf-105">エントリ識別子は、ASCII 文字列にエンコードします。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cfbf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2cfbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="2cfbf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2cfbf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2cfbf-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2cfbf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2cfbf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2cfbf-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-110">Called by:</span></span>  <br/> |<span data-ttu-id="2cfbf-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2cfbf-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="2cfbf-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="2cfbf-112">Parameters</span></span>

 <span data-ttu-id="2cfbf-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="2cfbf-113">_cb_</span></span>
  
> <span data-ttu-id="2cfbf-114">[in]_終了して_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="2cfbf-115">_終了して_</span><span class="sxs-lookup"><span data-stu-id="2cfbf-115">_pentry_</span></span>
  
> <span data-ttu-id="2cfbf-116">[in]エンコードするエントリの識別子を含む[エントリ ID](entryid.md)の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="2cfbf-117">_2 つ_</span><span class="sxs-lookup"><span data-stu-id="2cfbf-117">_psz_</span></span>
  
> <span data-ttu-id="2cfbf-118">[out]返される ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2cfbf-119">Return value</span><span class="sxs-lookup"><span data-stu-id="2cfbf-119">Return value</span></span>

<span data-ttu-id="2cfbf-120">なし。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2cfbf-121">備考</span><span class="sxs-lookup"><span data-stu-id="2cfbf-121">Remarks</span></span>

<span data-ttu-id="2cfbf-122">[HrEntryIDFromSz](hrentryidfromsz.md)と**HrSzFromEntryID**関数は、文字列とエントリの識別子のバイナリ フォーマット間の変換を提供します。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="2cfbf-123">MAPI では、バイナリ データを含む構造体を使用してください。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2cfbf-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2cfbf-124">Notes to callers</span></span>

<span data-ttu-id="2cfbf-125">**HrSzFromEntryID**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2cfbf-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

