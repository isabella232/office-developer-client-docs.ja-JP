---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ff46c58fbb352d56ae3df09d6949cdd5f614673f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800108"
---
# <a name="formprintsetup"></a><span data-ttu-id="a12ca-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="a12ca-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="a12ca-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a12ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a12ca-105">フォーム オブジェクトの印刷のセットアップ情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a12ca-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a12ca-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a12ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="a12ca-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a12ca-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a><span data-ttu-id="a12ca-108">Members</span><span class="sxs-lookup"><span data-stu-id="a12ca-108">Members</span></span>

 <span data-ttu-id="a12ca-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a12ca-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a12ca-110">文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a12ca-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="a12ca-111">次のフラグを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a12ca-111">The following flag can be used:</span></span>
    
<span data-ttu-id="a12ca-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a12ca-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a12ca-113">文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="a12ca-113">The strings are in Unicode format.</span></span> <span data-ttu-id="a12ca-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a12ca-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a12ca-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="a12ca-115">**hDevmode**</span></span>
  
> <span data-ttu-id="a12ca-116">プリンターのモードを処理します。</span><span class="sxs-lookup"><span data-stu-id="a12ca-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="a12ca-117">**と**</span><span class="sxs-lookup"><span data-stu-id="a12ca-117">**hDevnames**</span></span>
  
> <span data-ttu-id="a12ca-118">プリンターのパスを処理します。</span><span class="sxs-lookup"><span data-stu-id="a12ca-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="a12ca-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="a12ca-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="a12ca-120">印刷する最初のページのページ数です。</span><span class="sxs-lookup"><span data-stu-id="a12ca-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="a12ca-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="a12ca-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="a12ca-122">印刷する添付ファイルがあるかどうかを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="a12ca-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="a12ca-123">添付ファイルを印刷する場合は、 **ulFPrintAttachments**メンバーが 1 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a12ca-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="a12ca-124">印刷するのには添付ファイルがない場合は、0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a12ca-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a12ca-125">注釈</span><span class="sxs-lookup"><span data-stu-id="a12ca-125">Remarks</span></span>

<span data-ttu-id="a12ca-126">**FORMPRINTSETUP**構造体を使用して、フォーム オブジェクトの印刷のセットアップ情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="a12ca-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="a12ca-127">[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)の実装は、 **FORMPRINTSETUP**構造体を入力し、 **GetPrintSetup**の_lppFormPrintSetup_の出力パラメーターの内容に返します。</span><span class="sxs-lookup"><span data-stu-id="a12ca-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="a12ca-128">MAPI_UNICODE フラグが**GetPrintSetup**の_ulFlags_パラメーターで渡された場合は、 **hDevmode**および**と**のメンバーによって参照される文字列は Unicode 形式のはずです。</span><span class="sxs-lookup"><span data-stu-id="a12ca-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="a12ca-129">それ以外の場合、文字列は、ANSI 形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a12ca-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="a12ca-130">**IMAPIViewContext**を実装するフォームの閲覧者は[MAPIAllocateBuffer](mapiallocatebuffer.md)、MAPI アロケーター関数を使用する**FORMPRINTSETUP**構造体を割り当てる必要がありますが、 **hDevMode**および**と**、個々 のメンバーを割り当てるWindows 関数[調べます](http://go.microsoft.com/fwlink/?LinkId=132110)。</span><span class="sxs-lookup"><span data-stu-id="a12ca-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="a12ca-131">メモリのリリースは、同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a12ca-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="a12ca-132">[GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) Windows 関数を使用して[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して**FORMPRINTSETUP**構造体を解放する必要がありますが、 **hDevMode**および**と**のメンバーを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12ca-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a12ca-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a12ca-133">See also</span></span>



[<span data-ttu-id="a12ca-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="a12ca-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="a12ca-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a12ca-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a12ca-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a12ca-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="a12ca-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a12ca-137">MAPI Structures</span></span>](mapi-structures.md)

