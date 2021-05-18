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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327287"
---
# <a name="formprintsetup"></a><span data-ttu-id="70960-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="70960-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="70960-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70960-105">フォーム オブジェクトの印刷セットアップ情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="70960-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70960-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="70960-106">Header file:</span></span>  <br/> |<span data-ttu-id="70960-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="70960-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="70960-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="70960-108">Members</span></span>

 <span data-ttu-id="70960-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="70960-109">**ulFlags**</span></span>
  
> <span data-ttu-id="70960-110">文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="70960-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="70960-111">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="70960-111">The following flag can be used:</span></span>
    
<span data-ttu-id="70960-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70960-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70960-113">文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="70960-113">The strings are in Unicode format.</span></span> <span data-ttu-id="70960-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="70960-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="70960-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="70960-115">**hDevmode**</span></span>
  
> <span data-ttu-id="70960-116">プリンターのモードを処理します。</span><span class="sxs-lookup"><span data-stu-id="70960-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="70960-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="70960-117">**hDevnames**</span></span>
  
> <span data-ttu-id="70960-118">プリンターのパスを処理します。</span><span class="sxs-lookup"><span data-stu-id="70960-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="70960-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="70960-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="70960-120">印刷する最初のページのページ番号。</span><span class="sxs-lookup"><span data-stu-id="70960-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="70960-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="70960-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="70960-122">印刷する添付ファイルが含されているかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="70960-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="70960-123">印刷する添付ファイルがある場合 **、ulFPrintAttachments メンバー** は 1 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="70960-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="70960-124">印刷する添付ファイルがない場合は、0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="70960-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="70960-125">注釈</span><span class="sxs-lookup"><span data-stu-id="70960-125">Remarks</span></span>

<span data-ttu-id="70960-126">**FORMPRINTSETUP 構造** は、フォーム オブジェクトの印刷セットアップ情報を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="70960-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="70960-127">[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)の実装は **、FORMPRINTSETUP** 構造体に入力し **、GetPrintSetup** の _lppFormPrintSetup_ 出力パラメーターの内容で返します。</span><span class="sxs-lookup"><span data-stu-id="70960-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="70960-128">**GetPrintSetup** の _ulFlags_ パラメーターで MAPI_UNICODE フラグが渡される場合 **、hDevmode** メンバーと **hDevnames** メンバーによって参照される文字列は Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="70960-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="70960-129">それ以外の場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="70960-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="70960-130">**IMAPIViewContext** を実装するフォーム ビューアーは、MAPI アロケーター関数 [MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して **FORMPRINTSETUP** 構造体を割り当てる必要がありますが、Windows 関数 [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)を使用して個々のメンバー **hDevMode** および **hDevNames** を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70960-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="70960-131">メモリの解放も同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="70960-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="70960-132">**hDevMode** および **hDevNames** メンバーは、Windows 関数 [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108)を使用して解放する必要があります。一方 **、FORMPRINTSETUP** 構造体は [MAPIFreeBuffer](mapifreebuffer.md)関数で解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70960-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70960-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="70960-133">See also</span></span>



[<span data-ttu-id="70960-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="70960-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="70960-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="70960-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="70960-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="70960-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="70960-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="70960-137">MAPI Structures</span></span>](mapi-structures.md)

