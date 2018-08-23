---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800537"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="27836-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="27836-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="27836-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27836-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27836-105">フォームのコンテナーの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="27836-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="27836-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="27836-106">Parameters</span></span>

 <span data-ttu-id="27836-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27836-107">_ulFlags_</span></span>
  
> <span data-ttu-id="27836-108">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="27836-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="27836-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="27836-109">The following flag can be set:</span></span>
    
<span data-ttu-id="27836-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27836-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="27836-111">返される文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="27836-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="27836-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="27836-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="27836-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="27836-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="27836-114">[out]フォームのコンテナーの表示名を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="27836-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27836-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="27836-115">Return value</span></span>

<span data-ttu-id="27836-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="27836-116">S_OK</span></span> 
  
> <span data-ttu-id="27836-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="27836-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="27836-118">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="27836-118">MFCMAPI reference</span></span>

<span data-ttu-id="27836-119">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="27836-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="27836-120">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="27836-120">**File**</span></span>|<span data-ttu-id="27836-121">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="27836-121">**Function**</span></span>|<span data-ttu-id="27836-122">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="27836-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27836-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="27836-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="27836-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="27836-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="27836-125">MFCMAPI では、 **IMAPIFormContainer::GetDisplay**メソッドを使用して、CFormContainerDlg がレンダリングされるときに、フォームのコンテナーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="27836-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27836-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="27836-126">See also</span></span>



[<span data-ttu-id="27836-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27836-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="27836-128">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="27836-128">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

