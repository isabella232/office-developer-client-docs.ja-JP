---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800598"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="da114-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="da114-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="da114-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da114-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da114-105">現在のメッセージを作成または開いたの MAPI セッションを返します。</span><span class="sxs-lookup"><span data-stu-id="da114-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="da114-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="da114-106">Parameters</span></span>

 <span data-ttu-id="da114-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="da114-107">_ppSession_</span></span>
  
> <span data-ttu-id="da114-108">[out]返されたセッション オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="da114-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da114-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="da114-109">Return value</span></span>

<span data-ttu-id="da114-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="da114-110">S_OK</span></span> 
  
> <span data-ttu-id="da114-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="da114-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="da114-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="da114-112">S_FALSE</span></span> 
  
> <span data-ttu-id="da114-113">現在のメッセージのセッションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="da114-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da114-114">備考</span><span class="sxs-lookup"><span data-stu-id="da114-114">Remarks</span></span>

<span data-ttu-id="da114-115">フォームのサーバーに関連付けられているインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da114-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da114-116">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="da114-116">MFCMAPI reference</span></span>

<span data-ttu-id="da114-117">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="da114-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da114-118">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="da114-118">**File**</span></span>|<span data-ttu-id="da114-119">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="da114-119">**Function**</span></span>|<span data-ttu-id="da114-120">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="da114-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da114-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="da114-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="da114-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="da114-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="da114-123">MFCMAPI メソッドを使用して、 **IMAPIMessageSite::GetSession**現在キャッシュされているセッションのポインターを返すことがある場合。</span><span class="sxs-lookup"><span data-stu-id="da114-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da114-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="da114-124">See also</span></span>



[<span data-ttu-id="da114-125">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="da114-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="da114-126">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="da114-126">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

