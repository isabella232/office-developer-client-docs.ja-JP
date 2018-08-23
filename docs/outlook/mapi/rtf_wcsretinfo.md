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
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564963"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="d212a-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="d212a-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="d212a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d212a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d212a-105">この構造体は、ネイティブ形式の圧縮されたリッチ テキスト形式 (RTF) でカプセル化されたメッセージの本文を圧縮解除から返されるストリームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d212a-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d212a-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d212a-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="d212a-107">Members</span><span class="sxs-lookup"><span data-stu-id="d212a-107">Members</span></span>

<span data-ttu-id="d212a-108">_size_</span><span class="sxs-lookup"><span data-stu-id="d212a-108">_size_</span></span>
  
> <span data-ttu-id="d212a-109">バイト数で**この**構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="d212a-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="d212a-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="d212a-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="d212a-111">これは、ネイティブ形式の本文の形式を示す値です。</span><span class="sxs-lookup"><span data-stu-id="d212a-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="d212a-112">この値は[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される構造[について](rtf_wcsinfo.md)のパラメーター _ulFlags_に**MAPI_NATIVE_BODY**フラグが渡された場合。</span><span class="sxs-lookup"><span data-stu-id="d212a-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="d212a-113">次の値のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d212a-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="d212a-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="d212a-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="d212a-115">_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本体は、rtf 形式の場合、この値はのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d212a-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="d212a-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="d212a-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="d212a-117">_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本文は、テキスト形式の場合、この値はのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d212a-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="d212a-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="d212a-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="d212a-119">_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本体は、ハイパー テキスト マークアップ言語 (HTML) 形式の場合、この値はのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d212a-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d212a-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d212a-120">See also</span></span>

- [<span data-ttu-id="d212a-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="d212a-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

