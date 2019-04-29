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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411555"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="c5f78-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="c5f78-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="c5f78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5f78-105">エントリ識別子を ASCII 文字列にエンコードします。</span><span class="sxs-lookup"><span data-stu-id="c5f78-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5f78-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c5f78-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5f78-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="c5f78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c5f78-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c5f78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5f78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5f78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5f78-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c5f78-110">Called by:</span></span>  <br/> |<span data-ttu-id="c5f78-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c5f78-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="c5f78-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5f78-112">Parameters</span></span>

 <span data-ttu-id="c5f78-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="c5f78-113">_cb_</span></span>
  
> <span data-ttu-id="c5f78-114">順番_pentry_パラメーターによって指定されたエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="c5f78-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="c5f78-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="c5f78-115">_pentry_</span></span>
  
> <span data-ttu-id="c5f78-116">順番エンコードするエントリ識別子を含む[ENTRYID](entryid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5f78-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="c5f78-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="c5f78-117">_psz_</span></span>
  
> <span data-ttu-id="c5f78-118">読み上げ返された ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5f78-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5f78-119">Return value</span><span class="sxs-lookup"><span data-stu-id="c5f78-119">Return value</span></span>

<span data-ttu-id="c5f78-120">なし。</span><span class="sxs-lookup"><span data-stu-id="c5f78-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5f78-121">注釈</span><span class="sxs-lookup"><span data-stu-id="c5f78-121">Remarks</span></span>

<span data-ttu-id="c5f78-122">[HrEntryIDFromSz](hrentryidfromsz.md)および**hrszfromentryid**関数は、エントリ識別子の文字列形式とバイナリ形式の間の変換を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5f78-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="c5f78-123">MAPI では、バイナリデータで構造体を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5f78-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c5f78-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c5f78-124">Notes to callers</span></span>

<span data-ttu-id="c5f78-125">**hrszfromentryid**関数は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して ASCII 文字列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c5f78-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

