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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388904"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="81e46-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="81e46-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="81e46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81e46-105">呼び出し元のプロセスがメモリの指定された範囲に読み取りアクセス権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="81e46-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81e46-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="81e46-106">Header file:</span></span>  <br/> |<span data-ttu-id="81e46-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="81e46-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="81e46-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="81e46-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="81e46-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="81e46-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="81e46-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="81e46-110">Called by:</span></span>  <br/> |<span data-ttu-id="81e46-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="81e46-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="81e46-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81e46-112">Parameters</span></span>

 <span data-ttu-id="81e46-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="81e46-113">_lpsz_</span></span>
  
> <span data-ttu-id="81e46-114">[in]Null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81e46-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="81e46-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="81e46-115">_cchMax_</span></span>
  
> <span data-ttu-id="81e46-116">[in]文字数、文字列の最大サイズです。</span><span class="sxs-lookup"><span data-stu-id="81e46-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="81e46-117">関数は、文字列の終端の null 文字までのすべての文字の読み取りアクセス権のチェック、またはこのパラメーターで指定された文字の数は、どちらかが小さい。</span><span class="sxs-lookup"><span data-stu-id="81e46-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="81e46-118">このパラメーターが 0 の場合は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="81e46-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81e46-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="81e46-119">Return value</span></span>

<span data-ttu-id="81e46-120">呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権を持つ場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="81e46-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="81e46-121">呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権があるないときは、0 以外を返します。</span><span class="sxs-lookup"><span data-stu-id="81e46-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81e46-122">備考</span><span class="sxs-lookup"><span data-stu-id="81e46-122">Remarks</span></span>

<span data-ttu-id="81e46-123">**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用すると同じです。</span><span class="sxs-lookup"><span data-stu-id="81e46-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81e46-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="81e46-124">See also</span></span>



[<span data-ttu-id="81e46-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="81e46-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

