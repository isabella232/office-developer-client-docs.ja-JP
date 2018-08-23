---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801238"
---
# <a name="itnefsetprops"></a><span data-ttu-id="a29cf-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="a29cf-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="a29cf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a29cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a29cf-105">元のメッセージまたは添付ファイルを変更することがなくカプセル化されたメッセージまたは添付ファイルの 1 つまたは複数のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a29cf-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="a29cf-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a29cf-106">Parameters</span></span>

 <span data-ttu-id="a29cf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a29cf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a29cf-108">[in]プロパティの値を設定する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a29cf-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="a29cf-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a29cf-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a29cf-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="a29cf-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="a29cf-111">メッセージまたは添付ファイルの_ulElemID_パラメーターで指定されたプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="a29cf-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="a29cf-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="a29cf-112">_ulElemID_</span></span>
  
> <span data-ttu-id="a29cf-113">[in]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、一意にその数値が含まれていますが、親メッセージの添付ファイルを識別します。</span><span class="sxs-lookup"><span data-stu-id="a29cf-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="a29cf-114">_あう_</span><span class="sxs-lookup"><span data-stu-id="a29cf-114">_cValues_</span></span>
  
> <span data-ttu-id="a29cf-115">[in]_LpProps_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="a29cf-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="a29cf-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a29cf-116">_lpProps_</span></span>
  
> <span data-ttu-id="a29cf-117">[in]設定するプロパティのプロパティ値を含む**SPropValue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a29cf-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a29cf-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a29cf-118">Return value</span></span>

<span data-ttu-id="a29cf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a29cf-119">S_OK</span></span> 
  
> <span data-ttu-id="a29cf-120">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a29cf-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a29cf-121">注釈</span><span class="sxs-lookup"><span data-stu-id="a29cf-121">Remarks</span></span>

<span data-ttu-id="a29cf-122">プロバイダー、転送メッセージ ストア プロバイダーでは、プロパティを設定するのにはゲートウェイの呼び出し、 **ITnef::SetProps**メソッドに含める元のメッセージまたは添付ファイルを変更することがなく、メッセージまたは添付ファイルをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="a29cf-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="a29cf-123">この呼び出しで設定されたプロパティは、カプセル化されたメッセージ内の既存のプロパティをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="a29cf-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="a29cf-124">**SetProps**が[OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_ENCODE フラグを使用して開かれている TNEF オブジェクトに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a29cf-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="a29cf-125">プロパティの任意の数は、この呼び出しで設定できます。</span><span class="sxs-lookup"><span data-stu-id="a29cf-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a29cf-126">**SetProps**の実際の TNEF エンコードが行われないまで、 [ITnef::Finish](itnef-finish.md)メソッドが呼び出された後です。</span><span class="sxs-lookup"><span data-stu-id="a29cf-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="a29cf-127">**SetProps**に渡されたポインターに保つように有効期限**を終了**する呼び出しが行われた後、この機能を示します。</span><span class="sxs-lookup"><span data-stu-id="a29cf-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="a29cf-128">その時点で、すべてのオブジェクトと**SetProps**の呼び出しに渡されるデータは、リリースまたは解放されます。</span><span class="sxs-lookup"><span data-stu-id="a29cf-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a29cf-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a29cf-129">See also</span></span>



[<span data-ttu-id="a29cf-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="a29cf-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="a29cf-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a29cf-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="a29cf-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="a29cf-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="a29cf-133">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a29cf-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="a29cf-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a29cf-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="a29cf-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a29cf-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

