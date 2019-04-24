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
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278835"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="bf63d-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="bf63d-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="bf63d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf63d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf63d-105">呼び出し元プロセスが、指定されたメモリ範囲に対する読み取りアクセス権を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bf63d-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf63d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bf63d-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf63d-107">mapiwin</span><span class="sxs-lookup"><span data-stu-id="bf63d-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="bf63d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="bf63d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf63d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bf63d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bf63d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="bf63d-110">Called by:</span></span>  <br/> |<span data-ttu-id="bf63d-111">クライアントアプリケーションとサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="bf63d-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="bf63d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bf63d-112">Parameters</span></span>

 <span data-ttu-id="bf63d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="bf63d-113">_lpsz_</span></span>
  
> <span data-ttu-id="bf63d-114">順番null で終了する ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf63d-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="bf63d-115">_cchmax_</span><span class="sxs-lookup"><span data-stu-id="bf63d-115">_cchMax_</span></span>
  
> <span data-ttu-id="bf63d-116">順番文字列の最大サイズを文字数で指定します。</span><span class="sxs-lookup"><span data-stu-id="bf63d-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="bf63d-117">この関数は、文字列の終端の null 文字まで、またはこのパラメーターで指定された文字数までのすべての文字に対する読み取りアクセス権をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bf63d-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="bf63d-118">このパラメーターが0の場合、戻り値は0になります。</span><span class="sxs-lookup"><span data-stu-id="bf63d-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf63d-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="bf63d-119">Return value</span></span>

<span data-ttu-id="bf63d-120">呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持っている場合、戻り値は0です。または、 _cchmax_で指定された文字数まで読み出します。</span><span class="sxs-lookup"><span data-stu-id="bf63d-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="bf63d-121">戻り値は、呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持たない場合、または_cchmax_で指定された文字数までの読み取りアクセス権を持っていない場合は0以外の値です。</span><span class="sxs-lookup"><span data-stu-id="bf63d-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf63d-122">解説</span><span class="sxs-lookup"><span data-stu-id="bf63d-122">Remarks</span></span>

<span data-ttu-id="bf63d-123">**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="bf63d-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf63d-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf63d-124">See also</span></span>



[<span data-ttu-id="bf63d-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="bf63d-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

