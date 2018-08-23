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
ms.openlocfilehash: 81f9388b67d3194fe1442091b9f4f75a7671cb6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579649"
---
# <a name="itnefsetprops"></a><span data-ttu-id="7cc1d-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="7cc1d-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="7cc1d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cc1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cc1d-105">元のメッセージまたは添付ファイルを変更することがなくカプセル化されたメッセージまたは添付ファイルの 1 つまたは複数のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="7cc1d-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7cc1d-106">Parameters</span></span>

 <span data-ttu-id="7cc1d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cc1d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7cc1d-108">[in]プロパティの値を設定する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="7cc1d-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7cc1d-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="7cc1d-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="7cc1d-111">メッセージまたは添付ファイルの_ulElemID_パラメーターで指定されたプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="7cc1d-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="7cc1d-112">_ulElemID_</span></span>
  
> <span data-ttu-id="7cc1d-113">[in]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、一意にその数値が含まれていますが、親メッセージの添付ファイルを識別します。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="7cc1d-114">_あう_</span><span class="sxs-lookup"><span data-stu-id="7cc1d-114">_cValues_</span></span>
  
> <span data-ttu-id="7cc1d-115">[in]_LpProps_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="7cc1d-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="7cc1d-116">_lpProps_</span></span>
  
> <span data-ttu-id="7cc1d-117">[in]設定するプロパティのプロパティ値を含む**SPropValue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7cc1d-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7cc1d-118">Return value</span></span>

<span data-ttu-id="7cc1d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7cc1d-119">S_OK</span></span> 
  
> <span data-ttu-id="7cc1d-120">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cc1d-121">注釈</span><span class="sxs-lookup"><span data-stu-id="7cc1d-121">Remarks</span></span>

<span data-ttu-id="7cc1d-122">プロバイダー、転送メッセージ ストア プロバイダーでは、プロパティを設定するのにはゲートウェイの呼び出し、 **ITnef::SetProps**メソッドに含める元のメッセージまたは添付ファイルを変更することがなく、メッセージまたは添付ファイルをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="7cc1d-123">この呼び出しで設定されたプロパティは、カプセル化されたメッセージ内の既存のプロパティをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="7cc1d-124">**SetProps**が[OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_ENCODE フラグを使用して開かれている TNEF オブジェクトに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="7cc1d-125">プロパティの任意の数は、この呼び出しで設定できます。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7cc1d-126">**SetProps**の実際の TNEF エンコードが行われないまで、 [ITnef::Finish](itnef-finish.md)メソッドが呼び出された後です。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="7cc1d-127">**SetProps**に渡されたポインターに保つように有効期限**を終了**する呼び出しが行われた後、この機能を示します。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="7cc1d-128">その時点で、すべてのオブジェクトと**SetProps**の呼び出しに渡されるデータは、リリースまたは解放されます。</span><span class="sxs-lookup"><span data-stu-id="7cc1d-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7cc1d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7cc1d-129">See also</span></span>



[<span data-ttu-id="7cc1d-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="7cc1d-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="7cc1d-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="7cc1d-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="7cc1d-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="7cc1d-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="7cc1d-133">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7cc1d-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="7cc1d-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7cc1d-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="7cc1d-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cc1d-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

