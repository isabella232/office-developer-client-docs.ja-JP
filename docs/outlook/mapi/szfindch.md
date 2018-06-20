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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804074"
---
# <a name="szfindch"></a><span data-ttu-id="02c8d-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="02c8d-103">SzFindCh</span></span>
 
<span data-ttu-id="02c8d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02c8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02c8d-105">Null で終わる文字列内の文字の最初の出現箇所を検索します。</span><span class="sxs-lookup"><span data-stu-id="02c8d-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02c8d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="02c8d-106">Header file:</span></span>  <br/> |<span data-ttu-id="02c8d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02c8d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="02c8d-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="02c8d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="02c8d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="02c8d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="02c8d-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="02c8d-110">Called by:</span></span>  <br/> |<span data-ttu-id="02c8d-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="02c8d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="02c8d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="02c8d-112">Parameters</span></span>

<span data-ttu-id="02c8d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="02c8d-113">_lpsz_</span></span>
  
> <span data-ttu-id="02c8d-114">[in]検索する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="02c8d-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="02c8d-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="02c8d-115">_ch_</span></span>
  
> <span data-ttu-id="02c8d-116">[in]検索する文字。</span><span class="sxs-lookup"><span data-stu-id="02c8d-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02c8d-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="02c8d-117">Return value</span></span>

<span data-ttu-id="02c8d-118">**SzFindCh**は、最初に見つかった文字列の文字へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="02c8d-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="02c8d-119">文字が、文字列のどこにでも発生しない場合、または_lpsz_パラメーターが NULL の場合は、NULL 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="02c8d-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02c8d-120">備考</span><span class="sxs-lookup"><span data-stu-id="02c8d-120">Remarks</span></span>

<span data-ttu-id="02c8d-121">**SzFindCh**関数は、完全一致のみを検索します。このコマンドは、大文字と小文字やアクセントの違いに左右されます。</span><span class="sxs-lookup"><span data-stu-id="02c8d-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="02c8d-122">Unicode と DBCS の形式での検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="02c8d-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

