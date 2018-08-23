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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804074"
---
# <a name="szfindch"></a><span data-ttu-id="42654-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="42654-103">SzFindCh</span></span>
 
<span data-ttu-id="42654-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42654-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42654-105">Null で終わる文字列内の文字の最初の出現箇所を検索します。</span><span class="sxs-lookup"><span data-stu-id="42654-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42654-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="42654-106">Header file:</span></span>  <br/> |<span data-ttu-id="42654-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42654-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="42654-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="42654-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42654-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42654-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42654-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="42654-110">Called by:</span></span>  <br/> |<span data-ttu-id="42654-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="42654-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="42654-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="42654-112">Parameters</span></span>

<span data-ttu-id="42654-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="42654-113">_lpsz_</span></span>
  
> <span data-ttu-id="42654-114">[in]検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="42654-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="42654-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="42654-115">_ch_</span></span>
  
> <span data-ttu-id="42654-116">[in]検索する文字。</span><span class="sxs-lookup"><span data-stu-id="42654-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42654-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="42654-117">Return value</span></span>

<span data-ttu-id="42654-118">**SzFindCh**は、最初に見つかった文字列の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="42654-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="42654-119">文字が、文字列のどこにでも発生しない場合、または_lpsz_パラメーターが NULL の場合は、NULL 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="42654-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="42654-120">注釈</span><span class="sxs-lookup"><span data-stu-id="42654-120">Remarks</span></span>

<span data-ttu-id="42654-121">**SzFindCh**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。</span><span class="sxs-lookup"><span data-stu-id="42654-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="42654-122">Unicode と DBCS の形式での検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="42654-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

