---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800596"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="a61bd-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="a61bd-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="a61bd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a61bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a61bd-105">このようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。</span><span class="sxs-lookup"><span data-stu-id="a61bd-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="a61bd-106">埋め込まれたメッセージは、メッセージ ・ ストア内で直接の代わりに別のメッセージに格納されている_ppStore_パラメーターでは、このメソッドは NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="a61bd-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="a61bd-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a61bd-107">Parameters</span></span>

 <span data-ttu-id="a61bd-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="a61bd-108">_ppStore_</span></span>
  
> <span data-ttu-id="a61bd-109">[out]メッセージ ストアへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a61bd-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a61bd-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a61bd-110">Return value</span></span>

<span data-ttu-id="a61bd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a61bd-111">S_OK</span></span> 
  
> <span data-ttu-id="a61bd-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a61bd-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a61bd-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a61bd-113">S_FALSE</span></span> 
  
> <span data-ttu-id="a61bd-114">メッセージを格納しているストアはありません。</span><span class="sxs-lookup"><span data-stu-id="a61bd-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a61bd-115">備考</span><span class="sxs-lookup"><span data-stu-id="a61bd-115">Remarks</span></span>

<span data-ttu-id="a61bd-116">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a61bd-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a61bd-117">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="a61bd-117">MFCMAPI reference</span></span>

<span data-ttu-id="a61bd-118">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a61bd-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a61bd-119">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="a61bd-119">**File**</span></span>|<span data-ttu-id="a61bd-120">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="a61bd-120">**Function**</span></span>|<span data-ttu-id="a61bd-121">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="a61bd-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a61bd-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a61bd-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a61bd-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="a61bd-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="a61bd-124">MFCMAPI 使用可能になる場合に、指定されたストアに現在キャッシュされているポインターを取得する**IMAPIMessageSite::GetStore**メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a61bd-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a61bd-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a61bd-125">See also</span></span>



[<span data-ttu-id="a61bd-126">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a61bd-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="a61bd-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a61bd-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="a61bd-128">MAPI フォームのインタ フェース</span><span class="sxs-lookup"><span data-stu-id="a61bd-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

