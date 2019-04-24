---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315786"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="bb8ec-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="bb8ec-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="bb8ec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb8ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb8ec-105">この構造体は、圧縮リッチテキスト形式 (RTF) でカプセル化されたメッセージの本文を解凍することによって返されるネイティブ形式のストリームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bb8ec-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="bb8ec-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="bb8ec-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="bb8ec-107">Members</span></span>

<span data-ttu-id="bb8ec-108">_size_</span><span class="sxs-lookup"><span data-stu-id="bb8ec-108">_size_</span></span>
  
> <span data-ttu-id="bb8ec-109">**RTF_WCSRETINFO**構造体のサイズ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="bb8ec-110">_ulstreamflags_</span><span class="sxs-lookup"><span data-stu-id="bb8ec-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="bb8ec-111">これは、ネイティブ本文の形式を示す値です。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="bb8ec-112">この値は、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される[RTF_WCSINFO](rtf_wcsinfo.md)構造の_ulflags_パラメーターで**MAPI_NATIVE_BODY**フラグが渡された場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="bb8ec-113">次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="bb8ec-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="bb8ec-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="bb8ec-115">この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文が RTF の場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="bb8ec-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="bb8ec-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="bb8ec-117">この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文がプレーンテキスト形式の場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="bb8ec-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="bb8ec-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="bb8ec-119">この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文がハイパーテキストマークアップ言語 (HTML) 形式である場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb8ec-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb8ec-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb8ec-120">See also</span></span>

- [<span data-ttu-id="bb8ec-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="bb8ec-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

