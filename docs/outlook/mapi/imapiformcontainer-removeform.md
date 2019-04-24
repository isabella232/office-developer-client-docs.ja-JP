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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355745"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="c890c-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="c890c-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="c890c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c890c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c890c-105">フォームコンテナーから特定のフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="c890c-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="c890c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c890c-106">Parameters</span></span>

 <span data-ttu-id="c890c-107">_szmessageclass_</span><span class="sxs-lookup"><span data-stu-id="c890c-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="c890c-108">順番フォームコンテナーから削除するフォームのメッセージクラスの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="c890c-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="c890c-109">メッセージクラス名は常に ANSI 文字列で、Unicode はありません。</span><span class="sxs-lookup"><span data-stu-id="c890c-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c890c-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c890c-110">Return value</span></span>

<span data-ttu-id="c890c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c890c-111">S_OK</span></span> 
  
> <span data-ttu-id="c890c-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c890c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c890c-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c890c-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c890c-114">_szmessageclass_パラメーターで渡されたメッセージクラスが、フォームコンテナー内のフォームのメッセージクラスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="c890c-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c890c-115">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c890c-115">MFCMAPI reference</span></span>

<span data-ttu-id="c890c-116">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c890c-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c890c-117">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c890c-117">**File**</span></span>|<span data-ttu-id="c890c-118">**関数**</span><span class="sxs-lookup"><span data-stu-id="c890c-118">**Function**</span></span>|<span data-ttu-id="c890c-119">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c890c-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c890c-120">FormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="c890c-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="c890c-121">CFormContainerDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="c890c-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="c890c-122">mfcmapi は、 **imapiformcontainer:: removeform**メソッドを使用して、フォームコンテナーからフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="c890c-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c890c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c890c-123">See also</span></span>



[<span data-ttu-id="c890c-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c890c-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="c890c-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c890c-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

