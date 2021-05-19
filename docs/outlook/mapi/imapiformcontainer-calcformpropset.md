---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414915"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="e7e72-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="e7e72-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="e7e72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7e72-105">フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="e7e72-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="e7e72-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7e72-106">Parameters</span></span>

 <span data-ttu-id="e7e72-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7e72-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e7e72-108">[in]  _ppResults_ パラメーターのプロパティ配列がどのように返されるのか制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e7e72-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="e7e72-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e7e72-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="e7e72-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="e7e72-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="e7e72-111">返される配列には、フォームのプロパティの交差部分が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e7e72-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="e7e72-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="e7e72-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="e7e72-113">返される配列には、フォームのプロパティの共用体が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e7e72-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="e7e72-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7e72-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e7e72-115">配列で返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="e7e72-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="e7e72-116">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="e7e72-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e7e72-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="e7e72-117">_ppResults_</span></span>
  
> <span data-ttu-id="e7e72-118">[out]返される [SMAPIFormPropArray](smapiformproparray.md) 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="e7e72-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="e7e72-119">この構造には、インストールされているフォームで使用されるプロパティすべてが含まれる。</span><span class="sxs-lookup"><span data-stu-id="e7e72-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7e72-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="e7e72-120">Return value</span></span>

<span data-ttu-id="e7e72-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7e72-121">S_OK</span></span> 
  
> <span data-ttu-id="e7e72-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e7e72-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e7e72-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e7e72-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e7e72-124">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e7e72-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7e72-125">注釈</span><span class="sxs-lookup"><span data-stu-id="e7e72-125">Remarks</span></span>

<span data-ttu-id="e7e72-126">クライアント アプリケーションは **IMAPIFormContainer::CalcFormPropSet** メソッドを呼び出して、フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e7e72-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="e7e72-127">**IMAPIFormContainer::CalcFormPropSet** は [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) メソッドと同様に動作しますが、特定のコンテナーに登録されているフォームごとに動作します。</span><span class="sxs-lookup"><span data-stu-id="e7e72-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e7e72-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="e7e72-128">Notes to implementers</span></span>

<span data-ttu-id="e7e72-129">Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7e72-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7e72-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e7e72-130">Notes to callers</span></span>

 <span data-ttu-id="e7e72-131">**IMAPIFormContainer::CalcFormPropSet** は  _、ulFlags_ パラメーターで設定されたフラグに応じて、フォームのプロパティ セットの交差または共用体を取得し、結果のプロパティ グループを含む **SMAPIFormPropArray** 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="e7e72-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="e7e72-132">クライアントが  _ulFlags_ で MAPI_UNICODEフラグを渡す場合、返される文字列はすべて Unicode です。</span><span class="sxs-lookup"><span data-stu-id="e7e72-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7e72-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7e72-133">See also</span></span>



[<span data-ttu-id="e7e72-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="e7e72-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="e7e72-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="e7e72-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="e7e72-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7e72-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

