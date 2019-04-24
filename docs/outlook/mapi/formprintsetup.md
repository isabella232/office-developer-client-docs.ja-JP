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
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327287"
---
# <a name="formprintsetup"></a><span data-ttu-id="47e3a-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="47e3a-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="47e3a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47e3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47e3a-105">form オブジェクトの印刷設定情報を表します。</span><span class="sxs-lookup"><span data-stu-id="47e3a-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47e3a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="47e3a-106">Header file:</span></span>  <br/> |<span data-ttu-id="47e3a-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="47e3a-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="47e3a-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="47e3a-108">Members</span></span>

 <span data-ttu-id="47e3a-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="47e3a-109">**ulFlags**</span></span>
  
> <span data-ttu-id="47e3a-110">文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="47e3a-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="47e3a-111">次のフラグを使用できます。</span><span class="sxs-lookup"><span data-stu-id="47e3a-111">The following flag can be used:</span></span>
    
<span data-ttu-id="47e3a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47e3a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="47e3a-113">文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="47e3a-113">The strings are in Unicode format.</span></span> <span data-ttu-id="47e3a-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="47e3a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="47e3a-115">**hdevmode**</span><span class="sxs-lookup"><span data-stu-id="47e3a-115">**hDevmode**</span></span>
  
> <span data-ttu-id="47e3a-116">プリンターのモードを処理します。</span><span class="sxs-lookup"><span data-stu-id="47e3a-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="47e3a-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="47e3a-117">**hDevnames**</span></span>
  
> <span data-ttu-id="47e3a-118">プリンターのパスへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="47e3a-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="47e3a-119">**ulfirstpagenumber**</span><span class="sxs-lookup"><span data-stu-id="47e3a-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="47e3a-120">印刷する最初のページのページ番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="47e3a-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="47e3a-121">**ulfprintattachments**</span><span class="sxs-lookup"><span data-stu-id="47e3a-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="47e3a-122">印刷する添付ファイルがあるかどうかを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="47e3a-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="47e3a-123">印刷する添付ファイルがある場合、 **ulfprintattachments**メンバーは1に設定されます。</span><span class="sxs-lookup"><span data-stu-id="47e3a-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="47e3a-124">印刷する添付ファイルがない場合は、0に設定します。</span><span class="sxs-lookup"><span data-stu-id="47e3a-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47e3a-125">解説</span><span class="sxs-lookup"><span data-stu-id="47e3a-125">Remarks</span></span>

<span data-ttu-id="47e3a-126">**formprintsetup**構造は、form オブジェクトの印刷設定情報を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="47e3a-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="47e3a-127">[imapiviewcontext](imapiviewcontext-getprintsetup.md)の実装: getprintsetup は**formprintsetup**構造体に格納され、getprintsetup の_lppformprintsetup_出力パラメーターの内容\*\*\*\* で返されます。</span><span class="sxs-lookup"><span data-stu-id="47e3a-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="47e3a-128">**getprintsetup**の_ulflags_パラメーターで MAPI_UNICODE フラグが渡された場合、 **hdevmode**および**hDevnames**メンバーによって参照される文字列は、UNICODE 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="47e3a-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="47e3a-129">それ以外の場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="47e3a-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="47e3a-130">**imapiviewcontext**を実装するフォームビューアーでは、MAPI アロケーター関数[MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して**formprintsetup**構造体を割り当てる必要がありますが、個々のメンバー、 **hdevmode** 、 **hDevNames**を割り当てる必要があります。Windows 関数[GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)を使用します。</span><span class="sxs-lookup"><span data-stu-id="47e3a-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="47e3a-131">メモリの解放は同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="47e3a-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="47e3a-132">**hdevmode**メンバーと**hDevNames**メンバーは、Windows 関数[GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108)を使用して解放する必要がありますが、 **formprintsetup**構造体は[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47e3a-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47e3a-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="47e3a-133">See also</span></span>



[<span data-ttu-id="47e3a-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="47e3a-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="47e3a-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="47e3a-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="47e3a-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="47e3a-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="47e3a-137">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="47e3a-137">MAPI Structures</span></span>](mapi-structures.md)

