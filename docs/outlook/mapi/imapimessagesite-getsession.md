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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412689"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="0e02a-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="0e02a-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="0e02a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e02a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e02a-105">現在のメッセージが作成または開かされた MAPI セッションを返します。</span><span class="sxs-lookup"><span data-stu-id="0e02a-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="0e02a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e02a-106">Parameters</span></span>

 <span data-ttu-id="0e02a-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="0e02a-107">_ppSession_</span></span>
  
> <span data-ttu-id="0e02a-108">[out]返されたセッション オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="0e02a-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e02a-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e02a-109">Return value</span></span>

<span data-ttu-id="0e02a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e02a-110">S_OK</span></span> 
  
> <span data-ttu-id="0e02a-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0e02a-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0e02a-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0e02a-112">S_FALSE</span></span> 
  
> <span data-ttu-id="0e02a-113">現在のメッセージのセッションは存在しません。</span><span class="sxs-lookup"><span data-stu-id="0e02a-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e02a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0e02a-114">Remarks</span></span>

<span data-ttu-id="0e02a-115">フォーム サーバーに関連するインターフェイスの一覧については、「MAPI フォーム インターフェイス [」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="0e02a-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e02a-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0e02a-116">MFCMAPI reference</span></span>

<span data-ttu-id="0e02a-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e02a-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e02a-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e02a-118">**File**</span></span>|<span data-ttu-id="0e02a-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="0e02a-119">**Function**</span></span>|<span data-ttu-id="0e02a-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0e02a-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e02a-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0e02a-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0e02a-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="0e02a-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="0e02a-123">MFCMAPI では **、IMAPIMessageSite::GetSession** メソッドを使用して、現在キャッシュされているセッション ポインター (使用可能な場合) を返します。</span><span class="sxs-lookup"><span data-stu-id="0e02a-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e02a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e02a-124">See also</span></span>



[<span data-ttu-id="0e02a-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e02a-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="0e02a-126">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0e02a-126">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

