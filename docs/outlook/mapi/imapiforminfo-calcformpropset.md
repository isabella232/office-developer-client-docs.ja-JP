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
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="11c5e-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="11c5e-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="11c5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c5e-105">フォームが使用するプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="11c5e-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="11c5e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="11c5e-106">Parameters</span></span>

 <span data-ttu-id="11c5e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11c5e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="11c5e-108">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="11c5e-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="11c5e-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="11c5e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="11c5e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11c5e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="11c5e-111">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="11c5e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="11c5e-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="11c5e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="11c5e-113">_ppformproparray_</span><span class="sxs-lookup"><span data-stu-id="11c5e-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="11c5e-114">読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="11c5e-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="11c5e-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="11c5e-115">Return value</span></span>

<span data-ttu-id="11c5e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="11c5e-116">S_OK</span></span> 
  
> <span data-ttu-id="11c5e-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="11c5e-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="11c5e-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="11c5e-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="11c5e-119">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="11c5e-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="11c5e-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="11c5e-120">MFCMAPI reference</span></span>

<span data-ttu-id="11c5e-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11c5e-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="11c5e-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="11c5e-122">**File**</span></span>|<span data-ttu-id="11c5e-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="11c5e-123">**Function**</span></span>|<span data-ttu-id="11c5e-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="11c5e-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="11c5e-125">mfcoutput .cpp</span><span class="sxs-lookup"><span data-stu-id="11c5e-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="11c5e-126">出力 forminfo (_c)</span><span class="sxs-lookup"><span data-stu-id="11c5e-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="11c5e-127">mfcmapi は、フォーム情報オブジェクトのデバッグ出力を作成するときに**imapiforminfo:: CalcFormPropSet**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="11c5e-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11c5e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="11c5e-128">See also</span></span>



[<span data-ttu-id="11c5e-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="11c5e-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="11c5e-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="11c5e-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


<span data-ttu-id="11c5e-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="11c5e-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

