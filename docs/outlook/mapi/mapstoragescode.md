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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8dbb871a234d94f8bb2e21b15ce5de6f0db0e4ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581833"
---
# <a name="mapstoragescode"></a><span data-ttu-id="21903-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="21903-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="21903-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21903-105">SCODE のマップでは、HRESULT の種類に OLE ストレージ オブジェクトから値を返します。</span><span class="sxs-lookup"><span data-stu-id="21903-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21903-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="21903-106">Header file:</span></span>  <br/> |<span data-ttu-id="21903-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="21903-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="21903-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="21903-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="21903-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="21903-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="21903-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="21903-110">Called by:</span></span>  <br/> |<span data-ttu-id="21903-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="21903-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="21903-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21903-112">Parameters</span></span>

 <span data-ttu-id="21903-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="21903-113">_StgSCode_</span></span>
  
> <span data-ttu-id="21903-114">[in]SCODE の MAPI では、HRESULT の値にマップされる OLE ストレージ オブジェクトから値を返します。</span><span class="sxs-lookup"><span data-stu-id="21903-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21903-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="21903-115">Return value</span></span>

<span data-ttu-id="21903-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="21903-116">S_OK</span></span> 
  
> <span data-ttu-id="21903-117">呼び出しが成功し、予期される値が返されます。</span><span class="sxs-lookup"><span data-stu-id="21903-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="21903-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="21903-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="21903-119">関数は、一致する値を見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="21903-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21903-120">注釈</span><span class="sxs-lookup"><span data-stu-id="21903-120">Remarks</span></span>

<span data-ttu-id="21903-121">MAPI は、DLL のメッセージで、メッセージの実装を基本の MAPI コンポーネントの内部使用のため、 **MapStorageSCode**関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="21903-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="21903-122">これらのコンポーネント ファイルを開く OLE ストレージ自体、HRESULT 値を OLE ストレージの問題を返されるエラー値をマップできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="21903-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="21903-123">詳細については、[構造化ストレージ](structured-storage-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21903-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

