---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416525"
---
# <a name="mapstoragescode"></a><span data-ttu-id="e94bd-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="e94bd-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="e94bd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e94bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e94bd-105">マップ OLE ストレージ オブジェクトから HRESULT 型に SCODE 戻り値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e94bd-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e94bd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e94bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="e94bd-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e94bd-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e94bd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e94bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e94bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e94bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e94bd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e94bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="e94bd-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e94bd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="e94bd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e94bd-112">Parameters</span></span>

 <span data-ttu-id="e94bd-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="e94bd-113">_StgSCode_</span></span>
  
> <span data-ttu-id="e94bd-114">[in]HRESULT 値にマップする OLE ストレージ オブジェクトからの MAPI SCODE 戻り値。</span><span class="sxs-lookup"><span data-stu-id="e94bd-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e94bd-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="e94bd-115">Return value</span></span>

<span data-ttu-id="e94bd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e94bd-116">S_OK</span></span> 
  
> <span data-ttu-id="e94bd-117">呼び出しは成功し、予期される値を返しました。</span><span class="sxs-lookup"><span data-stu-id="e94bd-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="e94bd-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e94bd-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e94bd-119">関数は一致する値を見つけ出しません。</span><span class="sxs-lookup"><span data-stu-id="e94bd-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e94bd-120">注釈</span><span class="sxs-lookup"><span data-stu-id="e94bd-120">Remarks</span></span>

<span data-ttu-id="e94bd-121">MAPI は、メッセージの実装をメッセージ DLL に基付け、MAPI コンポーネントを内部的に使用する **MapStorageSCode** 関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="e94bd-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="e94bd-122">これらのコンポーネントは OLE ストレージ自体を開いているため、OLE ストレージの問題で返されるエラー値を HRESULT 値にマップできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e94bd-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="e94bd-123">詳細については[、「Structured Storage」 を参照してください](structured-storage-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="e94bd-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

