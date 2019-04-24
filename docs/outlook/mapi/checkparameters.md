---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332077"
---
# <a name="checkparameters"></a><span data-ttu-id="40d91-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="40d91-103">CheckParameters</span></span>

  
  
<span data-ttu-id="40d91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40d91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40d91-105">内部関数を呼び出して、MAPI によって呼び出されるサービスプロバイダーメソッドのデバッグパラメーターを検証します。</span><span class="sxs-lookup"><span data-stu-id="40d91-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40d91-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="40d91-106">Header file:</span></span>  <br/> |<span data-ttu-id="40d91-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="40d91-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="40d91-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="40d91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40d91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40d91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40d91-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="40d91-110">Called by:</span></span>  <br/> |<span data-ttu-id="40d91-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="40d91-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="40d91-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="40d91-112">Parameters</span></span>

 <span data-ttu-id="40d91-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="40d91-113">_eMethod_</span></span>
  
> <span data-ttu-id="40d91-114">順番検証するメソッドを列挙で指定します。</span><span class="sxs-lookup"><span data-stu-id="40d91-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="40d91-115">_First_</span><span class="sxs-lookup"><span data-stu-id="40d91-115">_First_</span></span>
  
> <span data-ttu-id="40d91-116">順番スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="40d91-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40d91-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="40d91-117">Return value</span></span>

<span data-ttu-id="40d91-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="40d91-118">S_OK</span></span> 
  
> <span data-ttu-id="40d91-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="40d91-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40d91-120">解説</span><span class="sxs-lookup"><span data-stu-id="40d91-120">Remarks</span></span>

<span data-ttu-id="40d91-121">checkparameters マクロによって**checkparameters**マクロ[](checkparms.md)が置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="40d91-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="40d91-122">**checkparms**は、すべてのプラットフォームで推奨されます。</span><span class="sxs-lookup"><span data-stu-id="40d91-122">**CheckParms** is recommended on all platforms.</span></span> 
  

