---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d0c044caf430c944d8912d050e4dbaba659c8b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582498"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="eb47d-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="eb47d-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="eb47d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb47d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb47d-105">フォームを使用するプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="eb47d-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="eb47d-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="eb47d-106">Parameters</span></span>

 <span data-ttu-id="eb47d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb47d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eb47d-108">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="eb47d-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="eb47d-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eb47d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="eb47d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb47d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eb47d-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="eb47d-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="eb47d-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="eb47d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="eb47d-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="eb47d-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="eb47d-114">[out]返された[SMAPIFormPropArray](smapiformproparray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb47d-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb47d-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="eb47d-115">Return value</span></span>

<span data-ttu-id="eb47d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb47d-116">S_OK</span></span> 
  
> <span data-ttu-id="eb47d-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="eb47d-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eb47d-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="eb47d-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="eb47d-119">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="eb47d-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="eb47d-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="eb47d-120">MFCMAPI reference</span></span>

<span data-ttu-id="eb47d-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="eb47d-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eb47d-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="eb47d-122">**File**</span></span>|<span data-ttu-id="eb47d-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="eb47d-123">**Function**</span></span>|<span data-ttu-id="eb47d-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="eb47d-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb47d-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="eb47d-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="eb47d-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="eb47d-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="eb47d-127">MFCMAPI は、オブジェクトの情報をフォームのデバッグ出力を作成するときに**IMAPIFormInfo::CalcFormPropSet**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb47d-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb47d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb47d-128">See also</span></span>



[<span data-ttu-id="eb47d-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="eb47d-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="eb47d-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="eb47d-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


<span data-ttu-id="eb47d-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="eb47d-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

