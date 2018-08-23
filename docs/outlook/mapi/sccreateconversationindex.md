---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803831"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="6ed45-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="6ed45-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="6ed45-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ed45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ed45-105">メッセージのスレッドでメッセージが属していることを示します。</span><span class="sxs-lookup"><span data-stu-id="6ed45-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ed45-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6ed45-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ed45-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6ed45-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6ed45-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6ed45-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ed45-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ed45-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ed45-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6ed45-110">Called by:</span></span>  <br/> |<span data-ttu-id="6ed45-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6ed45-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="6ed45-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6ed45-112">Parameters</span></span>

 <span data-ttu-id="6ed45-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="6ed45-113">_cbParent_</span></span>
  
> <span data-ttu-id="6ed45-114">[in]親スレッドのインデックス内のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="6ed45-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="6ed45-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="6ed45-115">_lpbParent_</span></span>
  
> <span data-ttu-id="6ed45-116">[in]親スレッドのインデックス内のバイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6ed45-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="6ed45-117">_CbParent_が 0 の場合、NULL があります。</span><span class="sxs-lookup"><span data-stu-id="6ed45-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="6ed45-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="6ed45-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="6ed45-119">[out]呼び出しによって返される新しい会話のインデックス内のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6ed45-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="6ed45-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="6ed45-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="6ed45-121">[out]呼び出しによって返される新しい会話のインデックスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6ed45-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ed45-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6ed45-122">Return value</span></span>

<span data-ttu-id="6ed45-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ed45-123">S_OK</span></span> 
  
> <span data-ttu-id="6ed45-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6ed45-124">The call succeeded and has returned the expected value or values.</span></span>
    

