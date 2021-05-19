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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435223"
---
# <a name="szfindsz"></a><span data-ttu-id="32090-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="32090-103">SzFindSz</span></span>

  
  
<span data-ttu-id="32090-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32090-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32090-105">null 終端文字列内の null 終端部分文字列の最初に出現する部分文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="32090-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32090-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="32090-106">Header file:</span></span>  <br/> |<span data-ttu-id="32090-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="32090-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="32090-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="32090-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="32090-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="32090-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="32090-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="32090-110">Called by:</span></span>  <br/> |<span data-ttu-id="32090-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="32090-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="32090-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32090-112">Parameters</span></span>

 <span data-ttu-id="32090-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="32090-113">_lpsz_</span></span>
  
> <span data-ttu-id="32090-114">[in]検索する null 終端文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="32090-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="32090-115">_lpsz パラメーター_ は、65536 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="32090-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="32090-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="32090-116">_lpszKey_</span></span>
  
> <span data-ttu-id="32090-117">[in]検索する null 終端部分文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="32090-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="32090-118">_lpszKey パラメーター_ は、65536 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="32090-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="32090-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="32090-119">Return value</span></span>

 <span data-ttu-id="32090-120">**SzFindSz** は、文字列内の部分文字列の最初に出現する文字の最初の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="32090-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="32090-121">文字列内の任意の場所で部分文字列が発生しない場合  _、lpszKey_ が  _lpsz_ より大きい場合、またはいずれかのパラメーターが NULL の場合は、NULL の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="32090-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32090-122">注釈</span><span class="sxs-lookup"><span data-stu-id="32090-122">Remarks</span></span>

<span data-ttu-id="32090-123">**SzFindSz** 関数は完全一致のみを検索します。大文字と小文字の違いには敏感です。</span><span class="sxs-lookup"><span data-stu-id="32090-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="32090-124">Unicode 形式と DBCS 形式の検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="32090-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="32090-125">両方のパラメーターの長さの制限は文字で、必ずしもバイトではありません。</span><span class="sxs-lookup"><span data-stu-id="32090-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

