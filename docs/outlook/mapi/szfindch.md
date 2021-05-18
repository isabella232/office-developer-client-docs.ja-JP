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
# <a name="szfindch"></a><span data-ttu-id="6dea5-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="6dea5-103">SzFindCh</span></span>
 
<span data-ttu-id="6dea5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dea5-105">null 終端文字列内の文字の最初の出現箇所を検索します。</span><span class="sxs-lookup"><span data-stu-id="6dea5-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6dea5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6dea5-106">Header file:</span></span>  <br/> |<span data-ttu-id="6dea5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dea5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6dea5-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6dea5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6dea5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6dea5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6dea5-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6dea5-110">Called by:</span></span>  <br/> |<span data-ttu-id="6dea5-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6dea5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="6dea5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6dea5-112">Parameters</span></span>

<span data-ttu-id="6dea5-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="6dea5-113">_lpsz_</span></span>
  
> <span data-ttu-id="6dea5-114">[in]検索する null 終端文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6dea5-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="6dea5-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="6dea5-115">_ch_</span></span>
  
> <span data-ttu-id="6dea5-116">[in]検索する文字。</span><span class="sxs-lookup"><span data-stu-id="6dea5-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dea5-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="6dea5-117">Return value</span></span>

<span data-ttu-id="6dea5-118">**SzFindCh** は、文字列内の文字の最初の出現位置へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="6dea5-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="6dea5-119">文字列内の任意の場所で文字が発生しない場合、または  _lpsz_ パラメーターが NULL の場合は、NULL の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6dea5-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6dea5-120">注釈</span><span class="sxs-lookup"><span data-stu-id="6dea5-120">Remarks</span></span>

<span data-ttu-id="6dea5-121">**SzFindCh** 関数は完全一致のみを検索します。大文字と小文字の違いには敏感です。</span><span class="sxs-lookup"><span data-stu-id="6dea5-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="6dea5-122">Unicode 形式と DBCS 形式の検索がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6dea5-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

