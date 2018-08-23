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
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594153"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="46355-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="46355-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="46355-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46355-105">メッセージのスレッドでメッセージが属していることを示します。</span><span class="sxs-lookup"><span data-stu-id="46355-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46355-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="46355-106">Header file:</span></span>  <br/> |<span data-ttu-id="46355-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="46355-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="46355-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="46355-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="46355-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="46355-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="46355-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46355-110">Called by:</span></span>  <br/> |<span data-ttu-id="46355-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="46355-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="46355-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="46355-112">Parameters</span></span>

 <span data-ttu-id="46355-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="46355-113">_cbParent_</span></span>
  
> <span data-ttu-id="46355-114">[in]親スレッドのインデックス内のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="46355-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="46355-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="46355-115">_lpbParent_</span></span>
  
> <span data-ttu-id="46355-116">[in]親スレッドのインデックス内のバイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="46355-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="46355-117">_CbParent_が 0 の場合、NULL があります。</span><span class="sxs-lookup"><span data-stu-id="46355-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="46355-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="46355-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="46355-119">[out]呼び出しによって返される新しい会話のインデックス内のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="46355-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="46355-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="46355-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="46355-121">[out]呼び出しによって返される新しい会話のインデックスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="46355-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46355-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="46355-122">Return value</span></span>

<span data-ttu-id="46355-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="46355-123">S_OK</span></span> 
  
> <span data-ttu-id="46355-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="46355-124">The call succeeded and has returned the expected value or values.</span></span>
    

