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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db3cc987b20a76116f2591485f57afae017d3e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567714"
---
# <a name="imapiforminfocalcverbset"></a><span data-ttu-id="c1588-103">IMAPIFormInfo::CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="c1588-103">IMAPIFormInfo::CalcVerbSet</span></span>

  
  
<span data-ttu-id="c1588-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1588-105">フォームを使用する動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c1588-105">Returns a pointer to the complete set of verbs that a form uses.</span></span>
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a><span data-ttu-id="c1588-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c1588-106">Parameters</span></span>

 <span data-ttu-id="c1588-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1588-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c1588-108">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c1588-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c1588-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c1588-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c1588-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1588-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c1588-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c1588-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c1588-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c1588-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c1588-113">_ppMAPIVerbArray_</span><span class="sxs-lookup"><span data-stu-id="c1588-113">_ppMAPIVerbArray_</span></span>
  
> <span data-ttu-id="c1588-114">[out]フォームの動詞が含まれている返された[SMAPIVerbArray](smapiverbarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1588-114">[out] A pointer to a pointer to the returned [SMAPIVerbArray](smapiverbarray.md) structure that contains the form's verbs.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c1588-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c1588-115">Return value</span></span>

<span data-ttu-id="c1588-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1588-116">S_OK</span></span> 
  
> <span data-ttu-id="c1588-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c1588-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c1588-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c1588-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c1588-119">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c1588-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1588-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c1588-120">Remarks</span></span>

<span data-ttu-id="c1588-121">クライアント アプリケーションは、フォームで使用されている動詞のセットへのポインターを取得する**IMAPIFormInfo::CalcVerbSet**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1588-121">Client applications call the **IMAPIFormInfo::CalcVerbSet** method to obtain a pointer to the set of verbs used by a form.</span></span> <span data-ttu-id="c1588-122">_PpMAPIVerbArray_パラメーターに返される**SMAPIVerbArray**構造で、動詞がインデックス番号の順に返されます。**lVerb**メンバーでは、各動詞のインデックスが検索されます。</span><span class="sxs-lookup"><span data-stu-id="c1588-122">In the **SMAPIVerbArray** structure returned in the  _ppMAPIVerbArray_ parameter, the verbs are returned in order of index number; each verb's index is found in its **lVerb** member.</span></span> <span data-ttu-id="c1588-123">クライアント アプリケーションでは、動的にメニューを作成、非表示にするまたはボタンを表示すると、動詞の配列を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1588-123">Client applications can use the verb array to dynamically build menus, hide or show buttons, and so on.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1588-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="c1588-124">MFCMAPI reference</span></span>

<span data-ttu-id="c1588-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="c1588-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1588-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="c1588-126">**File**</span></span>|<span data-ttu-id="c1588-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="c1588-127">**Function**</span></span>|<span data-ttu-id="c1588-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="c1588-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1588-129">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="c1588-129">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="c1588-130">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="c1588-130">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="c1588-131">MFCMAPI では、オブジェクトの情報をフォームのデバッグ出力の書き込み中に、 **IMAPIFormInfo::CalcVerbSet**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1588-131">MFCMAPI uses the **IMAPIFormInfo::CalcVerbSet** method while writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1588-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1588-132">See also</span></span>



[<span data-ttu-id="c1588-133">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="c1588-133">SMAPIVerbArray</span></span>](smapiverbarray.md)
  
[<span data-ttu-id="c1588-134">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1588-134">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


<span data-ttu-id="c1588-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c1588-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

