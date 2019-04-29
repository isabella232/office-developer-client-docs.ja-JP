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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425597"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="fe6d8-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="fe6d8-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="fe6d8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe6d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe6d8-105">1つ以上のエントリ (通常、メッセージングユーザー、配布リスト、またはその他のコンテナー) を削除します。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fe6d8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fe6d8-106">Parameters</span></span>

 <span data-ttu-id="fe6d8-107">_lpentries_</span><span class="sxs-lookup"><span data-stu-id="fe6d8-107">_lpEntries_</span></span>
  
> <span data-ttu-id="fe6d8-108">順番削除されるエントリを表すエントリ識別子を含む[entrylist](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="fe6d8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe6d8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fe6d8-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fe6d8-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fe6d8-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="fe6d8-111">Return value</span></span>

<span data-ttu-id="fe6d8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe6d8-112">S_OK</span></span> 
  
> <span data-ttu-id="fe6d8-113">指定したエントリが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="fe6d8-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="fe6d8-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="fe6d8-115">呼び出しは成功しましたが、1つ以上のエントリを削除できませんでした。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="fe6d8-116">この値が返されると、呼び出しが成功したとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="fe6d8-117">この値をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="fe6d8-118">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fe6d8-119">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fe6d8-119">MFCMAPI reference</span></span>

<span data-ttu-id="fe6d8-120">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fe6d8-121">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fe6d8-121">**File**</span></span>|<span data-ttu-id="fe6d8-122">**関数**</span><span class="sxs-lookup"><span data-stu-id="fe6d8-122">**Function**</span></span>|<span data-ttu-id="fe6d8-123">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fe6d8-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe6d8-124">abdlg .cpp</span><span class="sxs-lookup"><span data-stu-id="fe6d8-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="fe6d8-125">cabdlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="fe6d8-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="fe6d8-126">mfcmapi は、 **deleteentries**メソッドを使用して、アドレス帳コンテナーから特定のエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="fe6d8-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe6d8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe6d8-127">See also</span></span>



[<span data-ttu-id="fe6d8-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="fe6d8-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


<span data-ttu-id="fe6d8-129">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fe6d8-129">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

