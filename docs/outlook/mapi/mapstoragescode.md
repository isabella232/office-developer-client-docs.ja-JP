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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801547"
---
# <a name="mapstoragescode"></a><span data-ttu-id="e3b0f-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="e3b0f-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="e3b0f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3b0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3b0f-105">SCODE のマップでは、HRESULT の種類に OLE ストレージ オブジェクトから値を返します。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3b0f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e3b0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3b0f-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e3b0f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e3b0f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3b0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e3b0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e3b0f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e3b0f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e3b0f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="e3b0f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e3b0f-112">Parameters</span></span>

 <span data-ttu-id="e3b0f-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="e3b0f-113">_StgSCode_</span></span>
  
> <span data-ttu-id="e3b0f-114">[in]SCODE の MAPI では、HRESULT の値にマップされる OLE ストレージ オブジェクトから値を返します。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3b0f-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e3b0f-115">Return value</span></span>

<span data-ttu-id="e3b0f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3b0f-116">S_OK</span></span> 
  
> <span data-ttu-id="e3b0f-117">呼び出しが成功し、予期される値が返されます。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="e3b0f-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e3b0f-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e3b0f-119">関数は、一致する値を見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3b0f-120">備考</span><span class="sxs-lookup"><span data-stu-id="e3b0f-120">Remarks</span></span>

<span data-ttu-id="e3b0f-121">MAPI は、DLL のメッセージで、メッセージの実装を基本の MAPI コンポーネントの内部使用のため、 **MapStorageSCode**関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="e3b0f-122">これらのコンポーネント ファイルを開く OLE ストレージ自体、HRESULT 値を OLE ストレージの問題を返されるエラー値をマップできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="e3b0f-123">詳細については、[構造化ストレージ](structured-storage-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3b0f-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

