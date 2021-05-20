---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432199"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="aedae-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="aedae-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="aedae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aedae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aedae-105">フォーム コンテナーから特定のフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="aedae-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="aedae-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aedae-106">Parameters</span></span>

 <span data-ttu-id="aedae-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="aedae-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="aedae-108">[in]フォーム コンテナーから削除するフォームのメッセージ クラスを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="aedae-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="aedae-109">メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。</span><span class="sxs-lookup"><span data-stu-id="aedae-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aedae-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="aedae-110">Return value</span></span>

<span data-ttu-id="aedae-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="aedae-111">S_OK</span></span> 
  
> <span data-ttu-id="aedae-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="aedae-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="aedae-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aedae-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="aedae-114">_szMessageClass_ パラメーターで渡されたメッセージ クラスは、フォーム コンテナー内のフォームのメッセージ クラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="aedae-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="aedae-115">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="aedae-115">MFCMAPI reference</span></span>

<span data-ttu-id="aedae-116">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aedae-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aedae-117">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="aedae-117">**File**</span></span>|<span data-ttu-id="aedae-118">**関数**</span><span class="sxs-lookup"><span data-stu-id="aedae-118">**Function**</span></span>|<span data-ttu-id="aedae-119">**コメント**</span><span class="sxs-lookup"><span data-stu-id="aedae-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aedae-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aedae-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="aedae-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="aedae-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="aedae-122">MFCMAPI は **IMAPIFormContainer::RemoveForm** メソッドを使用してフォーム コンテナーからフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="aedae-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aedae-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="aedae-123">See also</span></span>



[<span data-ttu-id="aedae-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aedae-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="aedae-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="aedae-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

