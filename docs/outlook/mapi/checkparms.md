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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582036"
---
# <a name="checkparms"></a><span data-ttu-id="6e64a-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="6e64a-103">CheckParms</span></span>

  
  
<span data-ttu-id="6e64a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e64a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e64a-105">MAPI によって呼び出されるサービス プロバイダーのメソッドのデバッグ パラメーターを検証するために内部の関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e64a-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e64a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6e64a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e64a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6e64a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6e64a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6e64a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6e64a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6e64a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6e64a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6e64a-110">Called by:</span></span>  <br/> |<span data-ttu-id="6e64a-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6e64a-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="6e64a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e64a-112">Parameters</span></span>

 <span data-ttu-id="6e64a-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="6e64a-113">_eMethod_</span></span>
  
> <span data-ttu-id="6e64a-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e64a-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="6e64a-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="6e64a-115">_First_</span></span>
  
> <span data-ttu-id="6e64a-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6e64a-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e64a-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6e64a-117">Return value</span></span>

<span data-ttu-id="6e64a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e64a-118">S_OK</span></span> 
  
> <span data-ttu-id="6e64a-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="6e64a-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e64a-120">注釈</span><span class="sxs-lookup"><span data-stu-id="6e64a-120">Remarks</span></span>

<span data-ttu-id="6e64a-121">[ValidateParms](validateparms.md)と[UlValidateParms](ulvalidateparms.md)のマクロとは異なり、 **CheckParms**マクロでは、完全なパラメーターの検証は実行されません。</span><span class="sxs-lookup"><span data-stu-id="6e64a-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="6e64a-122">MAPI とサービスの間で渡されるパラメーター プロバイダーと見なされ、正しい**CheckParms**デバッグ検証のみを実行するようにします。</span><span class="sxs-lookup"><span data-stu-id="6e64a-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

