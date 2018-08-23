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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567595"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="4fd47-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="4fd47-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="4fd47-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fd47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fd47-105">エントリ識別子は、ASCII 文字列にエンコードします。</span><span class="sxs-lookup"><span data-stu-id="4fd47-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fd47-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4fd47-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fd47-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4fd47-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4fd47-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4fd47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fd47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4fd47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4fd47-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4fd47-110">Called by:</span></span>  <br/> |<span data-ttu-id="4fd47-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4fd47-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="4fd47-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4fd47-112">Parameters</span></span>

 <span data-ttu-id="4fd47-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="4fd47-113">_cb_</span></span>
  
> <span data-ttu-id="4fd47-114">[in]_終了して_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="4fd47-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="4fd47-115">_終了して_</span><span class="sxs-lookup"><span data-stu-id="4fd47-115">_pentry_</span></span>
  
> <span data-ttu-id="4fd47-116">[in]エンコードするエントリの識別子を含む[エントリ ID](entryid.md)の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4fd47-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="4fd47-117">_2 つ_</span><span class="sxs-lookup"><span data-stu-id="4fd47-117">_psz_</span></span>
  
> <span data-ttu-id="4fd47-118">[out]返される ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4fd47-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fd47-119">Return value</span><span class="sxs-lookup"><span data-stu-id="4fd47-119">Return value</span></span>

<span data-ttu-id="4fd47-120">なし。</span><span class="sxs-lookup"><span data-stu-id="4fd47-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fd47-121">注釈</span><span class="sxs-lookup"><span data-stu-id="4fd47-121">Remarks</span></span>

<span data-ttu-id="4fd47-122">[HrEntryIDFromSz](hrentryidfromsz.md)と**HrSzFromEntryID**関数は、文字列とエントリの識別子のバイナリ フォーマット間の変換を提供します。</span><span class="sxs-lookup"><span data-stu-id="4fd47-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="4fd47-123">MAPI では、バイナリ データを含む構造体を使用してください。</span><span class="sxs-lookup"><span data-stu-id="4fd47-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4fd47-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4fd47-124">Notes to callers</span></span>

<span data-ttu-id="4fd47-125">**HrSzFromEntryID**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4fd47-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

