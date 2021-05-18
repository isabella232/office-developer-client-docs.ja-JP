---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278835"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="1b1fd-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="1b1fd-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="1b1fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b1fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b1fd-105">呼び出し元のプロセスが、指定されたメモリ範囲への読み取りアクセス権を持っているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b1fd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1b1fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b1fd-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="1b1fd-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="1b1fd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="1b1fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b1fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b1fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b1fd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1b1fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="1b1fd-111">クライアント アプリケーションとサービス プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="1b1fd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b1fd-112">Parameters</span></span>

 <span data-ttu-id="1b1fd-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="1b1fd-113">_lpsz_</span></span>
  
> <span data-ttu-id="1b1fd-114">[in]NULL 終端 ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="1b1fd-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="1b1fd-115">_cchMax_</span></span>
  
> <span data-ttu-id="1b1fd-116">[in]文字列の最大サイズ (CHARs)。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="1b1fd-117">この関数は、文字列の終端の null 文字までのすべての文字、またはこのパラメーターで指定された文字数までの読み取りアクセスをチェックします。これより小さい方を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="1b1fd-118">このパラメーターが 0 の場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b1fd-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="1b1fd-119">Return value</span></span>

<span data-ttu-id="1b1fd-120">呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持つ場合、または  _cchMax_ で指定された文字数までの読み取りアクセス権を持つ場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="1b1fd-121">呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字への読み取りアクセス権を持たない場合、または  _cchMax_ で指定された文字数までの読み取りアクセス権がない場合、戻り値は 0 以外です。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b1fd-122">注釈</span><span class="sxs-lookup"><span data-stu-id="1b1fd-122">Remarks</span></span>

<span data-ttu-id="1b1fd-123">**IsBadBoundedStringPtr** 関数は **IsBadStringPtr の使用と同等です**。</span><span class="sxs-lookup"><span data-stu-id="1b1fd-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b1fd-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b1fd-124">See also</span></span>



[<span data-ttu-id="1b1fd-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="1b1fd-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

