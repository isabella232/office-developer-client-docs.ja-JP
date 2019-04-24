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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351325"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="38946-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="38946-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="38946-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38946-105">メッセージスレッドのメッセージが属する場所を示します。</span><span class="sxs-lookup"><span data-stu-id="38946-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38946-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="38946-106">Header file:</span></span>  <br/> |<span data-ttu-id="38946-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="38946-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="38946-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="38946-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38946-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38946-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38946-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="38946-110">Called by:</span></span>  <br/> |<span data-ttu-id="38946-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="38946-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="38946-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38946-112">Parameters</span></span>

 <span data-ttu-id="38946-113">_cbparent_</span><span class="sxs-lookup"><span data-stu-id="38946-113">_cbParent_</span></span>
  
> <span data-ttu-id="38946-114">順番親の会話インデックスのバイト数。</span><span class="sxs-lookup"><span data-stu-id="38946-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="38946-115">_lpbparent_</span><span class="sxs-lookup"><span data-stu-id="38946-115">_lpbParent_</span></span>
  
> <span data-ttu-id="38946-116">順番親スレッドのインデックス内のバイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="38946-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="38946-117">_cbparent_が0の場合、これは NULL になることがあります。</span><span class="sxs-lookup"><span data-stu-id="38946-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="38946-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="38946-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="38946-119">読み上げ呼び出しによって返される新しい会話インデックス内のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="38946-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="38946-120">_lppbindex_</span><span class="sxs-lookup"><span data-stu-id="38946-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="38946-121">読み上げ呼び出しによって返される新しい会話インデックスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="38946-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38946-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="38946-122">Return value</span></span>

<span data-ttu-id="38946-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="38946-123">S_OK</span></span> 
  
> <span data-ttu-id="38946-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="38946-124">The call succeeded and has returned the expected value or values.</span></span>
    

