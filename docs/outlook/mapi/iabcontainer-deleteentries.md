---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c744407790fecde6b6d89dff669ea4db07ce7701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800330"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="0691f-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="0691f-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="0691f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0691f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0691f-105">一般ユーザー、配布リスト、またはその他のコンテナーをメッセージング、1 つまたは複数のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="0691f-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0691f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0691f-106">Parameters</span></span>

 <span data-ttu-id="0691f-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="0691f-107">_lpEntries_</span></span>
  
> <span data-ttu-id="0691f-108">[in]削除されるエントリを表すエントリの識別子を含む[ENTRYLIST](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0691f-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="0691f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0691f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0691f-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0691f-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0691f-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0691f-111">Return value</span></span>

<span data-ttu-id="0691f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0691f-112">S_OK</span></span> 
  
> <span data-ttu-id="0691f-113">指定したエントリが削除されました。</span><span class="sxs-lookup"><span data-stu-id="0691f-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="0691f-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0691f-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0691f-115">呼び出しが成功したが、1 つまたは複数のエントリを削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="0691f-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="0691f-116">この値が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0691f-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="0691f-117">この値をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="0691f-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0691f-118">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0691f-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0691f-119">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0691f-119">MFCMAPI reference</span></span>

<span data-ttu-id="0691f-120">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0691f-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0691f-121">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0691f-121">**File**</span></span>|<span data-ttu-id="0691f-122">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0691f-122">**Function**</span></span>|<span data-ttu-id="0691f-123">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0691f-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0691f-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0691f-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="0691f-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="0691f-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="0691f-126">MFCMAPI では、 **DeleteEntries**メソッドを使用して、アドレス帳コンテナーから特定のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="0691f-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0691f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0691f-127">See also</span></span>



[<span data-ttu-id="0691f-128">これにより: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0691f-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


<span data-ttu-id="0691f-129">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0691f-129">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

