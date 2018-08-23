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
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567056"
---
# <a name="checkparameters"></a><span data-ttu-id="4bf7e-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="4bf7e-103">CheckParameters</span></span>

  
  
<span data-ttu-id="4bf7e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bf7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bf7e-105">MAPI によって呼び出されるサービス プロバイダーのメソッドのデバッグ パラメーターを検証するために内部の関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4bf7e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4bf7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="4bf7e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="4bf7e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="4bf7e-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4bf7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4bf7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4bf7e-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="4bf7e-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4bf7e-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="4bf7e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4bf7e-112">Parameters</span></span>

 <span data-ttu-id="4bf7e-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="4bf7e-113">_eMethod_</span></span>
  
> <span data-ttu-id="4bf7e-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="4bf7e-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="4bf7e-115">_First_</span></span>
  
> <span data-ttu-id="4bf7e-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4bf7e-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4bf7e-117">Return value</span></span>

<span data-ttu-id="4bf7e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bf7e-118">S_OK</span></span> 
  
> <span data-ttu-id="4bf7e-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bf7e-120">注釈</span><span class="sxs-lookup"><span data-stu-id="4bf7e-120">Remarks</span></span>

<span data-ttu-id="4bf7e-121">[CheckParms](checkparms.md)マクロでは、 **CheckParameters**マクロを置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="4bf7e-122">すべてのプラットフォームでは、 **CheckParms**をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4bf7e-122">**CheckParms** is recommended on all platforms.</span></span> 
  

