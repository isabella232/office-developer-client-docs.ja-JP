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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b15dc4e467644c2a0c3856372b550c3b55469f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800520"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="06b20-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="06b20-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="06b20-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06b20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06b20-105">フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="06b20-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="06b20-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="06b20-106">Parameters</span></span>

 <span data-ttu-id="06b20-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06b20-107">_ulFlags_</span></span>
  
> <span data-ttu-id="06b20-108">[in]_PpResults_パラメーターのプロパティの配列を返す方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="06b20-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="06b20-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="06b20-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="06b20-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="06b20-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="06b20-111">返される配列には、フォームのプロパティの積集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b20-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="06b20-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="06b20-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="06b20-113">返される配列には、フォームのプロパティの和集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b20-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="06b20-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06b20-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="06b20-115">配列で返される文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="06b20-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="06b20-116">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="06b20-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="06b20-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="06b20-117">_ppResults_</span></span>
  
> <span data-ttu-id="06b20-118">[out]返された[SMAPIFormPropArray](smapiformproparray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="06b20-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="06b20-119">この構造体には、インストールされているフォームで使用されるすべてのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b20-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="06b20-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="06b20-120">Return value</span></span>

<span data-ttu-id="06b20-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="06b20-121">S_OK</span></span> 
  
> <span data-ttu-id="06b20-122">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="06b20-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="06b20-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="06b20-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="06b20-124">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="06b20-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06b20-125">備考</span><span class="sxs-lookup"><span data-stu-id="06b20-125">Remarks</span></span>

<span data-ttu-id="06b20-126">クライアント アプリケーションは、フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得する**IMAPIFormContainer::CalcFormPropSet**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="06b20-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="06b20-127">**IMAPIFormContainer::CalcFormPropSet**は、特定のコンテナーに登録されているすべてのフォーム上で動作する点を除いて、 [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)メソッドと同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="06b20-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="06b20-128">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="06b20-128">Notes to implementers</span></span>

<span data-ttu-id="06b20-129">Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="06b20-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="06b20-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="06b20-130">Notes to callers</span></span>

 <span data-ttu-id="06b20-131">**IMAPIFormContainer::CalcFormPropSet**交差または_ulFlags_パラメーターに設定したフラグに応じて、フォームのプロパティのセットの和集合のいずれかは、含まれている**SMAPIFormPropArray**構造体が返されます、プロパティのグループを結果として得られる。</span><span class="sxs-lookup"><span data-stu-id="06b20-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="06b20-132">_UlFlags_で、クライアントが、MAPI_UNICODE フラグを渡すと、すべての関数が返す文字列は Unicode です。</span><span class="sxs-lookup"><span data-stu-id="06b20-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06b20-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="06b20-133">See also</span></span>



[<span data-ttu-id="06b20-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="06b20-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="06b20-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="06b20-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="06b20-136">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="06b20-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

