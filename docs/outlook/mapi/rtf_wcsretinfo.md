---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426171"
---
# <a name="rtf_wcsretinfo"></a><span data-ttu-id="1f139-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="1f139-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="1f139-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f139-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f139-105">この構造体は、圧縮リッチ テキスト形式 (RTF) でカプセル化されたメッセージの本文を圧縮解除して返されるネイティブ形式のストリームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f139-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1f139-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1f139-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="1f139-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="1f139-107">Members</span></span>

<span data-ttu-id="1f139-108">_size_</span><span class="sxs-lookup"><span data-stu-id="1f139-108">_size_</span></span>
  
> <span data-ttu-id="1f139-109">バイト **数RTF_WCSRETINFO構造体** のサイズです。</span><span class="sxs-lookup"><span data-stu-id="1f139-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="1f139-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="1f139-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="1f139-111">これは、ネイティブ本文の形式を示す値です。</span><span class="sxs-lookup"><span data-stu-id="1f139-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="1f139-112">この値は [、wrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される **RTF_WCSINFO** 構造体の _ulFlags_ パラメーターに [MAPI_NATIVE_BODY](rtf_wcsinfo.md)フラグが渡された場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="1f139-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="1f139-113">これには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1f139-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="1f139-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="1f139-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="1f139-115">この値は _、ulFlags_ にパラメーターフラグが含MAPI_NATIVE_BODY、本文が RTF の場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f139-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="1f139-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="1f139-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="1f139-117">この値は _、ulFlags_ に MAPI_NATIVE_BODYフラグが含まれる場合にのみ使用され、本文はプレーン テキスト形式です。</span><span class="sxs-lookup"><span data-stu-id="1f139-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="1f139-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="1f139-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="1f139-119">この値は _、ulFlags_ に MAPI_NATIVE_BODYフラグが含まれる場合にのみ使用され、本文はハイパーテキスト マークアップ言語 (HTML) 形式です。</span><span class="sxs-lookup"><span data-stu-id="1f139-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f139-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f139-120">See also</span></span>

- [<span data-ttu-id="1f139-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="1f139-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

