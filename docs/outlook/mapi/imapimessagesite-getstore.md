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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410470"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="1c206-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="1c206-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="1c206-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c206-105">そのようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。</span><span class="sxs-lookup"><span data-stu-id="1c206-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="1c206-106">このメソッドは、埋め込みメッセージの  _ppStore_ パラメーターに NULL を返します。これは、メッセージ ストアに直接ではなく、別のメッセージに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1c206-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="1c206-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c206-107">Parameters</span></span>

 <span data-ttu-id="1c206-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="1c206-108">_ppStore_</span></span>
  
> <span data-ttu-id="1c206-109">[out]メッセージ ストアへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="1c206-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c206-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c206-110">Return value</span></span>

<span data-ttu-id="1c206-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c206-111">S_OK</span></span> 
  
> <span data-ttu-id="1c206-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1c206-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1c206-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1c206-113">S_FALSE</span></span> 
  
> <span data-ttu-id="1c206-114">メッセージを含むストアはありません。</span><span class="sxs-lookup"><span data-stu-id="1c206-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c206-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1c206-115">Remarks</span></span>

<span data-ttu-id="1c206-116">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="1c206-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c206-117">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1c206-117">MFCMAPI reference</span></span>

<span data-ttu-id="1c206-118">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c206-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c206-119">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1c206-119">**File**</span></span>|<span data-ttu-id="1c206-120">**関数**</span><span class="sxs-lookup"><span data-stu-id="1c206-120">**Function**</span></span>|<span data-ttu-id="1c206-121">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1c206-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c206-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1c206-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1c206-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="1c206-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="1c206-124">MFCMAPI は **IMAPIMessageSite::GetStore** メソッドを使用して、現在キャッシュされているポインターを指定されたストア (使用可能な場合) に取得します。</span><span class="sxs-lookup"><span data-stu-id="1c206-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c206-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c206-125">See also</span></span>



[<span data-ttu-id="1c206-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c206-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="1c206-127">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1c206-127">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="1c206-128">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1c206-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

