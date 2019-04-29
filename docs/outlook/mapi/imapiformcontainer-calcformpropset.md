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
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="89dc3-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="89dc3-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="89dc3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89dc3-105">フォームコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="89dc3-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="89dc3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89dc3-106">Parameters</span></span>

 <span data-ttu-id="89dc3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89dc3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="89dc3-108">順番_ppResults_パラメーターのプロパティ配列を返す方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="89dc3-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="89dc3-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="89dc3-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="89dc3-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="89dc3-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="89dc3-111">返される配列には、フォームのプロパティの共通部分が含まれています。</span><span class="sxs-lookup"><span data-stu-id="89dc3-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="89dc3-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="89dc3-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="89dc3-113">返される配列には、フォームのプロパティの和集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="89dc3-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="89dc3-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89dc3-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="89dc3-115">配列で返される文字列は、Unicode 形式になっています。</span><span class="sxs-lookup"><span data-stu-id="89dc3-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="89dc3-116">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="89dc3-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="89dc3-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="89dc3-117">_ppResults_</span></span>
  
> <span data-ttu-id="89dc3-118">読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="89dc3-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="89dc3-119">この構造体には、インストールされているフォームで使用されるすべてのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="89dc3-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89dc3-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="89dc3-120">Return value</span></span>

<span data-ttu-id="89dc3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="89dc3-121">S_OK</span></span> 
  
> <span data-ttu-id="89dc3-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="89dc3-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="89dc3-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89dc3-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89dc3-124">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="89dc3-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89dc3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="89dc3-125">Remarks</span></span>

<span data-ttu-id="89dc3-126">クライアントアプリケーションは、 **imapiformcontainer:: CalcFormPropSet**メソッドを呼び出して、フォームコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="89dc3-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="89dc3-127">**imapiformcontainer:: CalcFormPropSet**は、 [imapiformcontainer:: CalcFormPropSet](imapiformmgr-calcformpropset.md)メソッドに似ていますが、特定のコンテナーに登録されているすべてのフォーム上で動作する点が異なります。</span><span class="sxs-lookup"><span data-stu-id="89dc3-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="89dc3-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="89dc3-128">Notes to implementers</span></span>

<span data-ttu-id="89dc3-129">Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="89dc3-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="89dc3-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="89dc3-130">Notes to callers</span></span>

 <span data-ttu-id="89dc3-131">**imapiformcontainer:: CalcFormPropSet**は、 _ulflags_パラメーターで設定されているフラグに応じて、フォームのプロパティセットの積集合またはユニオンを取得します。この構造体は、次の式を含む**smapiformproparray**結果のプロパティグループ。</span><span class="sxs-lookup"><span data-stu-id="89dc3-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="89dc3-132">クライアントが_ulflags_に MAPI_UNICODE フラグを渡すと、返されるすべての文字列は UNICODE になります。</span><span class="sxs-lookup"><span data-stu-id="89dc3-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89dc3-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="89dc3-133">See also</span></span>



[<span data-ttu-id="89dc3-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="89dc3-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="89dc3-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="89dc3-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="89dc3-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89dc3-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

