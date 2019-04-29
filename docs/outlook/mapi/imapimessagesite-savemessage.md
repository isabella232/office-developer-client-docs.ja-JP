---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417106"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="2530c-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="2530c-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="2530c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2530c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2530c-105">現在のメッセージを保存するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="2530c-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="2530c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2530c-106">Parameters</span></span>

<span data-ttu-id="2530c-107">なし。</span><span class="sxs-lookup"><span data-stu-id="2530c-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2530c-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="2530c-108">Return value</span></span>

<span data-ttu-id="2530c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="2530c-109">S_OK</span></span> 
  
> <span data-ttu-id="2530c-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2530c-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2530c-111">注釈</span><span class="sxs-lookup"><span data-stu-id="2530c-111">Remarks</span></span>

<span data-ttu-id="2530c-112">フォームは**IMAPIMessageSite:: SaveMessage**メソッドを呼び出して、メッセージの保存を要求します。</span><span class="sxs-lookup"><span data-stu-id="2530c-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="2530c-113">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2530c-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2530c-114">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2530c-114">MFCMAPI reference</span></span>

<span data-ttu-id="2530c-115">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2530c-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2530c-116">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2530c-116">**File**</span></span>|<span data-ttu-id="2530c-117">**関数**</span><span class="sxs-lookup"><span data-stu-id="2530c-117">**Function**</span></span>|<span data-ttu-id="2530c-118">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2530c-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2530c-119">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="2530c-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="2530c-120">cmymapiformviewer:: SaveMessage</span><span class="sxs-lookup"><span data-stu-id="2530c-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="2530c-121">mfcmapi は、 **IMAPIMessageSite:: SaveMessage**メソッドを使用してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="2530c-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2530c-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2530c-122">See also</span></span>



[<span data-ttu-id="2530c-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2530c-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="2530c-124">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2530c-124">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="2530c-125">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="2530c-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

