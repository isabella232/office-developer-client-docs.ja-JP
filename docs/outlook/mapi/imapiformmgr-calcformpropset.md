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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800539"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="14339-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="14339-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="14339-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14339-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14339-105">フォームのグループを使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="14339-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="14339-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14339-106">Parameters</span></span>

 <span data-ttu-id="14339-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="14339-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="14339-108">[in]プロパティを返す対象となるフォームを識別するオブジェクトのフォーム情報の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="14339-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="14339-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14339-109">_ulFlags_</span></span>
  
> <span data-ttu-id="14339-110">[in]_PpResults_パラメーターのプロパティの配列を返す方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="14339-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="14339-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="14339-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="14339-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="14339-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="14339-113">返される配列には、フォームのプロパティの積集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14339-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="14339-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="14339-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="14339-115">返される配列には、フォームのプロパティの和集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14339-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="14339-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="14339-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="14339-117">配列で返される文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="14339-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="14339-118">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="14339-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="14339-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="14339-119">_ppResults_</span></span>
  
> <span data-ttu-id="14339-120">[out]返された[SMAPIFormPropArray](smapiformproparray.md)構造体をフォームを使用するプロパティが含まれているへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="14339-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="14339-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="14339-121">Return value</span></span>

<span data-ttu-id="14339-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="14339-122">S_OK</span></span> 
  
> <span data-ttu-id="14339-123">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="14339-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="14339-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="14339-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="14339-125">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="14339-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14339-126">注釈</span><span class="sxs-lookup"><span data-stu-id="14339-126">Remarks</span></span>

<span data-ttu-id="14339-127">フォームの閲覧者は、フォームのグループを使用するプロパティの配列を取得する**IMAPIFormMgr::CalcFormPropSet**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="14339-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="14339-128">**CalcFormPropSet**には、交差、または共用体のこれらのフォームのプロパティ セットには、 _ulFlags_パラメーターとその設定のフラグによっての結果として得られるグループを格納する**SMAPIFormPropArray**構造体を返します。プロパティです。</span><span class="sxs-lookup"><span data-stu-id="14339-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="14339-129">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="14339-129">Notes to implementers</span></span>

<span data-ttu-id="14339-130">フォーム ビューアーでは、 _ulFlags_パラメーターに MAPI_UNICODE フラグが成功した場合のすべての文字列が Unicode の文字列として返されます。</span><span class="sxs-lookup"><span data-stu-id="14339-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="14339-131">Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="14339-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14339-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="14339-132">See also</span></span>



[<span data-ttu-id="14339-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="14339-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="14339-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14339-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

