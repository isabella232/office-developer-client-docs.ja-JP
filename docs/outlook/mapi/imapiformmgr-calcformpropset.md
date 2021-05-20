---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436427"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="5e06a-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="5e06a-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="5e06a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e06a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e06a-105">フォームのグループが使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="5e06a-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="5e06a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e06a-106">Parameters</span></span>

 <span data-ttu-id="5e06a-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="5e06a-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="5e06a-108">[in]プロパティを返すフォームを識別するフォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e06a-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="5e06a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e06a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5e06a-110">[in]  _ppResults_ パラメーターのプロパティ配列がどのように返されるのか制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5e06a-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="5e06a-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e06a-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="5e06a-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="5e06a-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="5e06a-113">返される配列には、フォームのプロパティの交差部分が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e06a-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="5e06a-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="5e06a-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="5e06a-115">返される配列には、フォームのプロパティの共用体が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5e06a-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="5e06a-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e06a-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e06a-117">配列で返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="5e06a-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="5e06a-118">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="5e06a-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5e06a-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="5e06a-119">_ppResults_</span></span>
  
> <span data-ttu-id="5e06a-120">[out]フォームが使用するプロパティを含む [、返される SMAPIFormPropArray](smapiformproparray.md) 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e06a-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e06a-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e06a-121">Return value</span></span>

<span data-ttu-id="5e06a-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e06a-122">S_OK</span></span> 
  
> <span data-ttu-id="5e06a-123">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="5e06a-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="5e06a-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5e06a-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5e06a-125">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5e06a-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e06a-126">注釈</span><span class="sxs-lookup"><span data-stu-id="5e06a-126">Remarks</span></span>

<span data-ttu-id="5e06a-127">フォーム ビューアーは **IMAPIFormMgr::CalcFormPropSet** メソッドを呼び出して、フォームのグループが使用するプロパティの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e06a-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="5e06a-128">**CalcFormPropSet** は  _、ulFlags_ パラメーターで設定されたフラグに応じて、これらのフォームのプロパティ セットの交差または共用体を取得し、結果のプロパティ グループを含む **SMAPIFormPropArray** 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="5e06a-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5e06a-129">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="5e06a-129">Notes to implementers</span></span>

<span data-ttu-id="5e06a-130">フォーム ビューアーが  _ulFlags_ パラメーター MAPI_UNICODEフラグを渡す場合、すべての文字列を Unicode 文字列として返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e06a-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="5e06a-131">Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e06a-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e06a-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e06a-132">See also</span></span>



[<span data-ttu-id="5e06a-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="5e06a-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="5e06a-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e06a-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

