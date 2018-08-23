---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39b4474bcc6bd71993fb5dc42bb2bfc1bf9f5f48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573405"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="6a911-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="6a911-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="6a911-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a911-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a911-105">呼び出し元のプロセスがメモリの指定された範囲に読み取りアクセス権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a911-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a911-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6a911-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a911-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="6a911-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="6a911-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6a911-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a911-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a911-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a911-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6a911-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a911-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="6a911-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="6a911-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a911-112">Parameters</span></span>

 <span data-ttu-id="6a911-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="6a911-113">_lpsz_</span></span>
  
> <span data-ttu-id="6a911-114">[in]Null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6a911-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="6a911-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="6a911-115">_cchMax_</span></span>
  
> <span data-ttu-id="6a911-116">[in]文字数、文字列の最大サイズです。</span><span class="sxs-lookup"><span data-stu-id="6a911-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="6a911-117">関数は、文字列の終端の null 文字までのすべての文字の読み取りアクセス権のチェック、またはこのパラメーターで指定された文字の数は、どちらかが小さい。</span><span class="sxs-lookup"><span data-stu-id="6a911-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="6a911-118">このパラメーターが 0 の場合は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="6a911-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a911-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a911-119">Return value</span></span>

<span data-ttu-id="6a911-120">呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権を持つ場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="6a911-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="6a911-121">呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権があるないときは、0 以外を返します。</span><span class="sxs-lookup"><span data-stu-id="6a911-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a911-122">注釈</span><span class="sxs-lookup"><span data-stu-id="6a911-122">Remarks</span></span>

<span data-ttu-id="6a911-123">**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用すると同じです。</span><span class="sxs-lookup"><span data-stu-id="6a911-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a911-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a911-124">See also</span></span>



[<span data-ttu-id="6a911-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="6a911-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

