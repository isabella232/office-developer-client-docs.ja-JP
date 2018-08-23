---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804076"
---
# <a name="szfindlastch"></a><span data-ttu-id="f8e67-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="f8e67-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="f8e67-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8e67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8e67-105">最後に出現する、null で終わる文字列内の文字を検索します。</span><span class="sxs-lookup"><span data-stu-id="f8e67-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8e67-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f8e67-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8e67-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8e67-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f8e67-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f8e67-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f8e67-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f8e67-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f8e67-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f8e67-110">Called by:</span></span>  <br/> |<span data-ttu-id="f8e67-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f8e67-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="f8e67-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e67-112">Parameters</span></span>

 <span data-ttu-id="f8e67-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="f8e67-113">_lpsz_</span></span>
  
> <span data-ttu-id="f8e67-114">[in]検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f8e67-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="f8e67-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="f8e67-115">_ch_</span></span>
  
> <span data-ttu-id="f8e67-116">[in]検索する文字。</span><span class="sxs-lookup"><span data-stu-id="f8e67-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8e67-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e67-117">Return value</span></span>

 <span data-ttu-id="f8e67-118">**SzFindLastCh**は、最後に見つかった文字列の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f8e67-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="f8e67-119">文字が、文字列のどこにでも発生しない場合、または_lpsz_パラメーターが NULL の場合は、NULL 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f8e67-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8e67-120">注釈</span><span class="sxs-lookup"><span data-stu-id="f8e67-120">Remarks</span></span>

<span data-ttu-id="f8e67-121">**SzFindLastCh**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。</span><span class="sxs-lookup"><span data-stu-id="f8e67-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="f8e67-122">Unicode と DBCS の形式での検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f8e67-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

