---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78fb610c5afc3cac4f6de84240f734e5ae196110
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565544"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="9bb4f-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="9bb4f-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="9bb4f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bb4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bb4f-105">このようなフォルダーが存在する場合は、フォルダーを現在のメッセージを作成または開いたを返します。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="9bb4f-106">このメソッドは、埋め込みメッセージは、フォルダーに直接格納されていないために_ppFolder_パラメーターで NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="9bb4f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9bb4f-107">Parameters</span></span>

 <span data-ttu-id="9bb4f-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="9bb4f-108">_ppFolder_</span></span>
  
> <span data-ttu-id="9bb4f-109">[out]返されるフォルダーへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9bb4f-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9bb4f-110">Return value</span></span>

<span data-ttu-id="9bb4f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bb4f-111">S_OK</span></span> 
  
> <span data-ttu-id="9bb4f-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9bb4f-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9bb4f-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9bb4f-113">S_FALSE</span></span> 
  
> <span data-ttu-id="9bb4f-114">メッセージのフォルダーが存在しません。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bb4f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="9bb4f-115">Remarks</span></span>

<span data-ttu-id="9bb4f-116">フォームのサーバーに関連付けられているインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9bb4f-117">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9bb4f-117">MFCMAPI reference</span></span>

<span data-ttu-id="9bb4f-118">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9bb4f-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9bb4f-119">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9bb4f-119">**File**</span></span>|<span data-ttu-id="9bb4f-120">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9bb4f-120">**Function**</span></span>|<span data-ttu-id="9bb4f-121">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9bb4f-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9bb4f-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="9bb4f-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9bb4f-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="9bb4f-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="9bb4f-124">MFCMAPI では、 **IMAPIMessageSite::GetFolder**メソッドを使用して、指定したフォルダーに現在キャッシュされているポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9bb4f-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bb4f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bb4f-125">See also</span></span>



[<span data-ttu-id="9bb4f-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bb4f-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="9bb4f-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9bb4f-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="9bb4f-128">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9bb4f-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

