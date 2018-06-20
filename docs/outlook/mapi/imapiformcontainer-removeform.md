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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800519"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="40915-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="40915-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="40915-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40915-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40915-105">特定のフォームは、フォームのコンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="40915-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="40915-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="40915-106">Parameters</span></span>

 <span data-ttu-id="40915-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="40915-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="40915-108">[in]フォームのコンテナーから削除するフォームのメッセージ クラスの名前を示す文字列です。</span><span class="sxs-lookup"><span data-stu-id="40915-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="40915-109">メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。</span><span class="sxs-lookup"><span data-stu-id="40915-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40915-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="40915-110">Return value</span></span>

<span data-ttu-id="40915-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="40915-111">S_OK</span></span> 
  
> <span data-ttu-id="40915-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="40915-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="40915-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="40915-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="40915-114">_SzMessageClass_パラメーターで渡されたメッセージ クラスでは、フォームのコンテナー内の任意のフォームのメッセージ クラスが一致しません。</span><span class="sxs-lookup"><span data-stu-id="40915-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="40915-115">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="40915-115">MFCMAPI reference</span></span>

<span data-ttu-id="40915-116">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="40915-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40915-117">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="40915-117">**File**</span></span>|<span data-ttu-id="40915-118">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="40915-118">**Function**</span></span>|<span data-ttu-id="40915-119">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="40915-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40915-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="40915-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="40915-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="40915-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="40915-122">MFCMAPI では、 **IMAPIFormContainer::RemoveForm**メソッドを使用して、フォームをフォームのコンテナーから削除します。</span><span class="sxs-lookup"><span data-stu-id="40915-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40915-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="40915-123">See also</span></span>



[<span data-ttu-id="40915-124">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="40915-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="40915-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="40915-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

