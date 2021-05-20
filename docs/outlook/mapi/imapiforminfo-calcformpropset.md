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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b62c21348da71c1ee863f70d6e6a549a5d10003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438072"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="c897c-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c897c-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="c897c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c897c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c897c-105">フォームで使用されるプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c897c-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="c897c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c897c-106">Parameters</span></span>

 <span data-ttu-id="c897c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c897c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c897c-108">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c897c-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c897c-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c897c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c897c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c897c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c897c-111">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="c897c-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c897c-112">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="c897c-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c897c-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="c897c-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="c897c-114">[out]返される [SMAPIFormPropArray](smapiformproparray.md) 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="c897c-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c897c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c897c-115">Return value</span></span>

<span data-ttu-id="c897c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c897c-116">S_OK</span></span> 
  
> <span data-ttu-id="c897c-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c897c-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c897c-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c897c-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c897c-119">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c897c-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c897c-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c897c-120">MFCMAPI reference</span></span>

<span data-ttu-id="c897c-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c897c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c897c-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c897c-122">**File**</span></span>|<span data-ttu-id="c897c-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="c897c-123">**Function**</span></span>|<span data-ttu-id="c897c-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c897c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c897c-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="c897c-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="c897c-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="c897c-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="c897c-127">MFCMAPI は、フォーム情報オブジェクトのデバッグ出力を記述するときに **IMAPIFormInfo::CalcFormPropSet** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c897c-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c897c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c897c-128">See also</span></span>



[<span data-ttu-id="c897c-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="c897c-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="c897c-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c897c-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


<span data-ttu-id="c897c-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c897c-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

