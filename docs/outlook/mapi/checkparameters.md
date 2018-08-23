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
ms.openlocfilehash: a693c06d933c7e93d384aac8da8d5311eaf1d9da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799815"
---
# <a name="checkparameters"></a><span data-ttu-id="d7dc6-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="d7dc6-103">CheckParameters</span></span>

  
  
<span data-ttu-id="d7dc6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7dc6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7dc6-105">MAPI によって呼び出されるサービス プロバイダーのメソッドのデバッグ パラメーターを検証するために内部の関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7dc6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d7dc6-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7dc6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d7dc6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d7dc6-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7dc6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7dc6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7dc6-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7dc6-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d7dc6-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="d7dc6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7dc6-112">Parameters</span></span>

 <span data-ttu-id="d7dc6-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="d7dc6-113">_eMethod_</span></span>
  
> <span data-ttu-id="d7dc6-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="d7dc6-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="d7dc6-115">_First_</span></span>
  
> <span data-ttu-id="d7dc6-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7dc6-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d7dc6-117">Return value</span></span>

<span data-ttu-id="d7dc6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7dc6-118">S_OK</span></span> 
  
> <span data-ttu-id="d7dc6-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7dc6-120">注釈</span><span class="sxs-lookup"><span data-stu-id="d7dc6-120">Remarks</span></span>

<span data-ttu-id="d7dc6-121">[CheckParms](checkparms.md)マクロでは、 **CheckParameters**マクロを置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="d7dc6-122">すべてのプラットフォームでは、 **CheckParms**をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d7dc6-122">**CheckParms** is recommended on all platforms.</span></span> 
  

