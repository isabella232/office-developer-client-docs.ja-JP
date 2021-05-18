---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422279"
---
# <a name="checkparms"></a><span data-ttu-id="a0152-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="a0152-103">CheckParms</span></span>

  
  
<span data-ttu-id="a0152-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0152-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0152-105">MAPI によって呼び出されるサービス プロバイダー メソッドのデバッグ パラメーターを検証する内部関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0152-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0152-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a0152-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0152-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a0152-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a0152-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a0152-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0152-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a0152-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a0152-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a0152-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0152-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a0152-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="a0152-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0152-112">Parameters</span></span>

 <span data-ttu-id="a0152-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="a0152-113">_eMethod_</span></span>
  
> <span data-ttu-id="a0152-114">[in]列挙で検証するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0152-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="a0152-115">_First_</span><span class="sxs-lookup"><span data-stu-id="a0152-115">_First_</span></span>
  
> <span data-ttu-id="a0152-116">[in]スタックの最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0152-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0152-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a0152-117">Return value</span></span>

<span data-ttu-id="a0152-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0152-118">S_OK</span></span> 
  
> <span data-ttu-id="a0152-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="a0152-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0152-120">注釈</span><span class="sxs-lookup"><span data-stu-id="a0152-120">Remarks</span></span>

<span data-ttu-id="a0152-121">[ValidateParms](validateparms.md)マクロと [UlValidateParms](ulvalidateparms.md)マクロとは対照的に **、CheckParms** マクロは完全なパラメーター検証を実行しません。</span><span class="sxs-lookup"><span data-stu-id="a0152-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="a0152-122">MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされます。 **そのため、CheckParms は** デバッグ検証のみを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0152-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

