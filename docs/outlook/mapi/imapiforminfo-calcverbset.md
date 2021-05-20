---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428782"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="32872-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="32872-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="32872-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32872-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32872-105">フォームで使用される動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="32872-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="32872-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32872-106">Parameters</span></span>

 <span data-ttu-id="32872-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32872-107">_ulFlags_</span></span>
  
> <span data-ttu-id="32872-108">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="32872-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="32872-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="32872-109">The following flag can be set:</span></span>
    
<span data-ttu-id="32872-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="32872-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="32872-111">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="32872-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="32872-112">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="32872-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="32872-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="32872-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="32872-114">[out]フォームの動詞を含む [、返される SMAPIVerbArray](smapiverbarray.md) 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="32872-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="32872-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="32872-115">Return value</span></span>

<span data-ttu-id="32872-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="32872-116">S_OK</span></span> 
  
> <span data-ttu-id="32872-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="32872-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="32872-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="32872-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="32872-119">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="32872-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32872-120">注釈</span><span class="sxs-lookup"><span data-stu-id="32872-120">Remarks</span></span>

<span data-ttu-id="32872-121">クライアント アプリケーションは **IMAPIFormInfo::CalcVerbSet** メソッドを呼び出して、フォームで使用される一連の動詞へのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="32872-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="32872-122">ppMAPIVerbArray パラメーターで返される _SMAPIVerbArray_ 構造体では、動詞はインデックス番号の順に返されます。 各動詞のインデックスは、**その lVerb メンバーに見** つかりました。</span><span class="sxs-lookup"><span data-stu-id="32872-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="32872-123">クライアント アプリケーションでは、動詞配列を使用してメニューを動的に作成したり、ボタンを非表示または表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="32872-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="32872-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="32872-124">MFCMAPI reference</span></span>

<span data-ttu-id="32872-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32872-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="32872-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="32872-126">**File**</span></span>|<span data-ttu-id="32872-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="32872-127">**Function**</span></span>|<span data-ttu-id="32872-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="32872-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32872-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="32872-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="32872-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="32872-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="32872-131">MFCMAPI は、フォーム情報オブジェクトのデバッグ出力を書き込む間に **IMAPIFormInfo::CalcVerbSet** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="32872-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32872-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="32872-132">See also</span></span>



[<span data-ttu-id="32872-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="32872-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="32872-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="32872-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


<span data-ttu-id="32872-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="32872-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

