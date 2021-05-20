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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430792"
---
# <a name="itnefsetprops"></a><span data-ttu-id="7295f-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="7295f-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="7295f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7295f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7295f-105">元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの 1 つ以上のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7295f-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="7295f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7295f-106">Parameters</span></span>

 <span data-ttu-id="7295f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7295f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7295f-108">[in]プロパティ値の設定方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7295f-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="7295f-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7295f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7295f-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="7295f-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="7295f-111">_ulElemID_ パラメーターで指定されたメッセージまたは添付ファイルのプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="7295f-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="7295f-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="7295f-112">_ulElemID_</span></span>
  
> <span data-ttu-id="7295f-113">[in]添付ファイル **のPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティで、親メッセージ内の添付ファイルを一意に識別する番号が含まれる。</span><span class="sxs-lookup"><span data-stu-id="7295f-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="7295f-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7295f-114">_cValues_</span></span>
  
> <span data-ttu-id="7295f-115">[in]_lpProps_ パラメーターが指す [SPropValue](spropvalue.md)構造体のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="7295f-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="7295f-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="7295f-116">_lpProps_</span></span>
  
> <span data-ttu-id="7295f-117">[in]設定するプロパティのプロパティ値を含む **SPropValue** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7295f-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7295f-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="7295f-118">Return value</span></span>

<span data-ttu-id="7295f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7295f-119">S_OK</span></span> 
  
> <span data-ttu-id="7295f-120">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="7295f-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7295f-121">注釈</span><span class="sxs-lookup"><span data-stu-id="7295f-121">Remarks</span></span>

<span data-ttu-id="7295f-122">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::SetProps** メソッドを呼び出して、元のメッセージまたは添付ファイルを変更せずに、メッセージまたは添付ファイルのカプセル化に含めるプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7295f-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="7295f-123">この呼び出しで設定されたプロパティは、カプセル化されたメッセージ内の既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="7295f-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="7295f-124">**SetProps** は [、OpenTnefStream または OpenTnefStreamEx](opentnefstream.md) 関数の TNEF_ENCODE フラグで開いた TNEF オブジェクトでのみ [サポート](opentnefstreamex.md) されます。</span><span class="sxs-lookup"><span data-stu-id="7295f-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="7295f-125">この呼び出しでは、任意の数のプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7295f-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7295f-126">[ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまで **、SetProps** の実際の TNEF エンコードは実行されません。</span><span class="sxs-lookup"><span data-stu-id="7295f-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="7295f-127">この機能は **、SetProps** に渡されるポインターは、Finish の呼び出しが行われた後まで有効なまま **である必要があります** 。</span><span class="sxs-lookup"><span data-stu-id="7295f-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="7295f-128">その時点で **、SetProps** 呼び出しに渡されるオブジェクトとデータはすべて解放または解放できます。</span><span class="sxs-lookup"><span data-stu-id="7295f-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7295f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7295f-129">See also</span></span>



[<span data-ttu-id="7295f-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="7295f-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="7295f-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="7295f-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="7295f-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="7295f-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="7295f-133">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7295f-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="7295f-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7295f-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="7295f-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7295f-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

