---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5b34e2c21ac967b0874872986c0cf484750f4e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804168"
---
# <a name="ulrelease"></a><span data-ttu-id="0b207-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="0b207-103">UlRelease</span></span>

  
  
<span data-ttu-id="0b207-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b207-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b207-105">**** OLE メソッドを呼び出す別の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b207-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b207-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0b207-106">Header file:</span></span>  <br/> |<span data-ttu-id="0b207-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b207-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0b207-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0b207-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0b207-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0b207-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0b207-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0b207-110">Called by:</span></span>  <br/> |<span data-ttu-id="0b207-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0b207-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="0b207-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0b207-112">Parameters</span></span>

 <span data-ttu-id="0b207-113">_パンク_</span><span class="sxs-lookup"><span data-stu-id="0b207-113">_punk_</span></span>
  
> <span data-ttu-id="0b207-114">[in]インターフェイスへのポインターは、任意の MAPI インターフェイスに、 **IUnknown**インターフェイスから派生します。</span><span class="sxs-lookup"><span data-stu-id="0b207-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0b207-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0b207-115">Return value</span></span>

<span data-ttu-id="0b207-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b207-116">S_OK</span></span> 
  
> <span data-ttu-id="0b207-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0b207-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0b207-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0b207-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0b207-119">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="0b207-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b207-120">備考</span><span class="sxs-lookup"><span data-stu-id="0b207-120">Remarks</span></span>

<span data-ttu-id="0b207-121">参照カウントは、既存のポインターを解放するオブジェクトの数です。</span><span class="sxs-lookup"><span data-stu-id="0b207-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="0b207-122">_Punk_パラメーターが NULL の場合は、**リ ス**を呼び出さずに、関数は直ちに戻ります</span><span class="sxs-lookup"><span data-stu-id="0b207-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="0b207-123">**UlRelease**は、リリースするオブジェクトの参照カウントと同じにすることができます**が**メソッドによって返される値を返します。</span><span class="sxs-lookup"><span data-stu-id="0b207-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="0b207-124">**リ ス**の詳細については、 [IUnknown インターフェイスを実装する](implementing-the-iunknown-interface.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b207-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

