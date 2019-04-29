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
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="7ba0e-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7ba0e-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="7ba0e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ba0e-105">フォームのグループが使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="7ba0e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7ba0e-106">Parameters</span></span>

 <span data-ttu-id="7ba0e-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="7ba0e-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="7ba0e-108">順番プロパティを返すフォームを識別するフォーム情報オブジェクトの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="7ba0e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ba0e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7ba0e-110">順番_ppResults_パラメーターのプロパティ配列を返す方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="7ba0e-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="7ba0e-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="7ba0e-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="7ba0e-113">返される配列には、フォームのプロパティの共通部分が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="7ba0e-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="7ba0e-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="7ba0e-115">返される配列には、フォームのプロパティの和集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="7ba0e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7ba0e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7ba0e-117">配列で返される文字列は、Unicode 形式になっています。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="7ba0e-118">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7ba0e-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="7ba0e-119">_ppResults_</span></span>
  
> <span data-ttu-id="7ba0e-120">読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。これには、フォームで使用するプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ba0e-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="7ba0e-121">Return value</span></span>

<span data-ttu-id="7ba0e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ba0e-122">S_OK</span></span> 
  
> <span data-ttu-id="7ba0e-123">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="7ba0e-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7ba0e-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7ba0e-125">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ba0e-126">注釈</span><span class="sxs-lookup"><span data-stu-id="7ba0e-126">Remarks</span></span>

<span data-ttu-id="7ba0e-127">フォーム閲覧者は、 **imapiformmgr:: CalcFormPropSet**メソッドを呼び出して、フォームのグループが使用するプロパティの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="7ba0e-128">**CalcFormPropSet**は、 _ulflags_パラメーターで設定されているフラグに応じて、これらのフォームのプロパティセットの積集合または和集合を受け取り、結果として得られるグループを含む**smapiformproparray**の構造を返します。プロパティ.</span><span class="sxs-lookup"><span data-stu-id="7ba0e-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7ba0e-129">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7ba0e-129">Notes to implementers</span></span>

<span data-ttu-id="7ba0e-130">フォームビューアーが_ulflags_パラメーターの MAPI_UNICODE フラグを渡す場合は、すべての文字列が UNICODE 文字列として返されます。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="7ba0e-131">Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="7ba0e-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ba0e-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ba0e-132">See also</span></span>



[<span data-ttu-id="7ba0e-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="7ba0e-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="7ba0e-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ba0e-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

