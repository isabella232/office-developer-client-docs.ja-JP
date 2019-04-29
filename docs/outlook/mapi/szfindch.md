---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421943"
---
# <a name="szfindch"></a><span data-ttu-id="8d06d-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="8d06d-103">SzFindCh</span></span>
 
<span data-ttu-id="8d06d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d06d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d06d-105">null で終了する文字列内で最初に見つかった文字を検索します。</span><span class="sxs-lookup"><span data-stu-id="8d06d-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d06d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8d06d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d06d-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d06d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8d06d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="8d06d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d06d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8d06d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8d06d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="8d06d-110">Called by:</span></span>  <br/> |<span data-ttu-id="8d06d-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="8d06d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="8d06d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d06d-112">Parameters</span></span>

<span data-ttu-id="8d06d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="8d06d-113">_lpsz_</span></span>
  
> <span data-ttu-id="8d06d-114">順番検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d06d-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="8d06d-115">_焦げ_</span><span class="sxs-lookup"><span data-stu-id="8d06d-115">_ch_</span></span>
  
> <span data-ttu-id="8d06d-116">順番検索する文字を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d06d-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d06d-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d06d-117">Return value</span></span>

<span data-ttu-id="8d06d-118">**szfindch**は、文字列内で最初に見つかった文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8d06d-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="8d06d-119">文字が文字列の任意の場所に出現しない場合、または_lpsz_パラメーターが null の場合は、null 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="8d06d-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d06d-120">注釈</span><span class="sxs-lookup"><span data-stu-id="8d06d-120">Remarks</span></span>

<span data-ttu-id="8d06d-121">**szfindch**関数は、完全一致のみを検索します。大文字と小文字は区別されます。</span><span class="sxs-lookup"><span data-stu-id="8d06d-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="8d06d-122">Unicode および DBCS 形式での検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8d06d-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

