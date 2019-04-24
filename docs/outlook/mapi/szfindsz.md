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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345746"
---
# <a name="szfindsz"></a><span data-ttu-id="427ec-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="427ec-103">SzFindSz</span></span>

  
  
<span data-ttu-id="427ec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="427ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="427ec-105">null で終わる部分文字列が、null で終了する文字列内で最初に見つかった部分を検索します。</span><span class="sxs-lookup"><span data-stu-id="427ec-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="427ec-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="427ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="427ec-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="427ec-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="427ec-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="427ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="427ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="427ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="427ec-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="427ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="427ec-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="427ec-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="427ec-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="427ec-112">Parameters</span></span>

 <span data-ttu-id="427ec-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="427ec-113">_lpsz_</span></span>
  
> <span data-ttu-id="427ec-114">順番検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="427ec-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="427ec-115">_lpsz_パラメーターは、65536文字以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="427ec-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="427ec-116">_lpszkey_</span><span class="sxs-lookup"><span data-stu-id="427ec-116">_lpszKey_</span></span>
  
> <span data-ttu-id="427ec-117">順番検索する null で終わるサブ文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="427ec-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="427ec-118">_lpszkey_パラメーターは、65536文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="427ec-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="427ec-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="427ec-119">Return value</span></span>

 <span data-ttu-id="427ec-120">**szfindsz**は、文字列内で最初に見つかった部分文字列の最初の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="427ec-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="427ec-121">substring_キー_が_lpsz_より大きい場合、またはいずれかのパラメーターが null の場合、文字列内の任意の場所にサブ文字列が含まれていない場合は、null 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="427ec-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="427ec-122">解説</span><span class="sxs-lookup"><span data-stu-id="427ec-122">Remarks</span></span>

<span data-ttu-id="427ec-123">**szfindsz**関数は、完全一致のみを検索します。大文字と小文字は区別されます。</span><span class="sxs-lookup"><span data-stu-id="427ec-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="427ec-124">Unicode および DBCS 形式での検索はサポートされています。</span><span class="sxs-lookup"><span data-stu-id="427ec-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="427ec-125">両方のパラメーターの長さ制限は、文字である必要があり、必ずしもバイトではありません。</span><span class="sxs-lookup"><span data-stu-id="427ec-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

