---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585123"
---
# <a name="szfindsz"></a><span data-ttu-id="6eea4-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="6eea4-103">SzFindSz</span></span>

  
  
<span data-ttu-id="6eea4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eea4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eea4-105">Null で終わる文字列で、null で終わる文字列の最初に見つかった位置を検索します。</span><span class="sxs-lookup"><span data-stu-id="6eea4-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6eea4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6eea4-106">Header file:</span></span>  <br/> |<span data-ttu-id="6eea4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6eea4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6eea4-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6eea4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6eea4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6eea4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6eea4-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6eea4-110">Called by:</span></span>  <br/> |<span data-ttu-id="6eea4-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6eea4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="6eea4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6eea4-112">Parameters</span></span>

 <span data-ttu-id="6eea4-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="6eea4-113">_lpsz_</span></span>
  
> <span data-ttu-id="6eea4-114">[in]検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6eea4-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="6eea4-115">_Lpsz_パラメーターは、65536 文字を超えない必要があります。</span><span class="sxs-lookup"><span data-stu-id="6eea4-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="6eea4-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="6eea4-116">_lpszKey_</span></span>
  
> <span data-ttu-id="6eea4-117">[in]検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6eea4-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="6eea4-118">_LpszKey_パラメーターは、65536 文字を超えない必要があります。</span><span class="sxs-lookup"><span data-stu-id="6eea4-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6eea4-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="6eea4-119">Return value</span></span>

 <span data-ttu-id="6eea4-120">**SzFindSz**は、最初に見つかった文字列の部分文字列の最初の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="6eea4-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="6eea4-121">部分文字列が発生しない場合任意の場所で、文字列_lpsz_より大きい場合は_lpszKey_またはどちらかのパラメーターが NULL の場合、NULL 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6eea4-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6eea4-122">注釈</span><span class="sxs-lookup"><span data-stu-id="6eea4-122">Remarks</span></span>

<span data-ttu-id="6eea4-123">**SzFindSz**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。</span><span class="sxs-lookup"><span data-stu-id="6eea4-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="6eea4-124">Unicode と DBCS の形式での検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6eea4-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="6eea4-125">両方のパラメーターの長さの制限は、文字数、バイト数ではありませんが。</span><span class="sxs-lookup"><span data-stu-id="6eea4-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

