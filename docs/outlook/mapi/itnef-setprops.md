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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315051"
---
# <a name="itnefsetprops"></a><span data-ttu-id="94de6-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="94de6-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="94de6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94de6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94de6-105">元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの1つ以上のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="94de6-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="94de6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94de6-106">Parameters</span></span>

 <span data-ttu-id="94de6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94de6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="94de6-108">順番プロパティ値の設定方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="94de6-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="94de6-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="94de6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="94de6-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="94de6-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="94de6-111">_ulの id_パラメーターで指定されたメッセージまたは添付ファイルからのプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="94de6-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="94de6-112">_ulの id_</span><span class="sxs-lookup"><span data-stu-id="94de6-112">_ulElemID_</span></span>
  
> <span data-ttu-id="94de6-113">順番添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティ。親メッセージの添付ファイルを一意に識別する番号を含みます。</span><span class="sxs-lookup"><span data-stu-id="94de6-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="94de6-114">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="94de6-114">_cValues_</span></span>
  
> <span data-ttu-id="94de6-115">順番_lpprops_パラメーターによってポイントされている[spropvalue](spropvalue.md)構造のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="94de6-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="94de6-116">_lpprops_</span><span class="sxs-lookup"><span data-stu-id="94de6-116">_lpProps_</span></span>
  
> <span data-ttu-id="94de6-117">順番設定するプロパティのプロパティ値を含む**spropvalue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94de6-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="94de6-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="94de6-118">Return value</span></span>

<span data-ttu-id="94de6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="94de6-119">S_OK</span></span> 
  
> <span data-ttu-id="94de6-120">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="94de6-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94de6-121">解説</span><span class="sxs-lookup"><span data-stu-id="94de6-121">Remarks</span></span>

<span data-ttu-id="94de6-122">トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: setprops**メソッドを呼び出して、元のメッセージまたは添付ファイルを変更せずに、メッセージまたは添付ファイルのカプセル化に含めるプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="94de6-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="94de6-123">この呼び出しで設定されたプロパティは、カプセル化されたメッセージの既存のプロパティより優先されます。</span><span class="sxs-lookup"><span data-stu-id="94de6-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="94de6-124">**setprops**は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して開かれた TNEF オブジェクトに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="94de6-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="94de6-125">この呼び出しでは、任意の数のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="94de6-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="94de6-126">[ITnef:: Finish](itnef-finish.md)メソッドが呼び出されるまで、 **setprops**の実際の TNEF エンコードは行われません。</span><span class="sxs-lookup"><span data-stu-id="94de6-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="94de6-127">この機能は、 **setprops**に渡されたポインターが、呼び出しが**完了**するまで有効なままである必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="94de6-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="94de6-128">この時点で、 **setprops**呼び出しに渡されたすべてのオブジェクトとデータを解放または解放することができます。</span><span class="sxs-lookup"><span data-stu-id="94de6-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94de6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="94de6-129">See also</span></span>



[<span data-ttu-id="94de6-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="94de6-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="94de6-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="94de6-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="94de6-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="94de6-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="94de6-133">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94de6-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="94de6-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="94de6-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="94de6-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94de6-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

