---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315373"
---
# <a name="uladdref"></a><span data-ttu-id="2fd05-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="2fd05-103">UlAddRef</span></span>

  
  
<span data-ttu-id="2fd05-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fd05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fd05-105">OLE メソッド**IUnknown:: AddRef**を呼び出すための別の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="2fd05-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fd05-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2fd05-106">Header file:</span></span>  <br/> |<span data-ttu-id="2fd05-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fd05-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2fd05-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="2fd05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2fd05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2fd05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2fd05-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2fd05-110">Called by:</span></span>  <br/> |<span data-ttu-id="2fd05-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2fd05-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="2fd05-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2fd05-112">Parameters</span></span>

 <span data-ttu-id="2fd05-113">_パンク_</span><span class="sxs-lookup"><span data-stu-id="2fd05-113">_punk_</span></span>
  
> <span data-ttu-id="2fd05-114">順番**IUnknown**インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="2fd05-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2fd05-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="2fd05-115">Return value</span></span>

<span data-ttu-id="2fd05-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fd05-116">S_OK</span></span> 
  
> <span data-ttu-id="2fd05-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2fd05-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="2fd05-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="2fd05-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="2fd05-119">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="2fd05-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fd05-120">解説</span><span class="sxs-lookup"><span data-stu-id="2fd05-120">Remarks</span></span>

 <span data-ttu-id="2fd05-121">**uladdref**は、 **IUnknown:: AddRef**メソッドによって返された値を返します。これは、インターフェイスの参照カウントの新しい値です。</span><span class="sxs-lookup"><span data-stu-id="2fd05-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="2fd05-122">値は0以外の値です。</span><span class="sxs-lookup"><span data-stu-id="2fd05-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="2fd05-123">**iunknown:: AddRef**の詳細については、「 [iunknown インターフェイスを実装する](implementing-the-iunknown-interface.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2fd05-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

