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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572306"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="b402a-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="b402a-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="b402a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b402a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b402a-105">現在のメッセージを保存するように要求します。</span><span class="sxs-lookup"><span data-stu-id="b402a-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="b402a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b402a-106">Parameters</span></span>

<span data-ttu-id="b402a-107">なし。</span><span class="sxs-lookup"><span data-stu-id="b402a-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b402a-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b402a-108">Return value</span></span>

<span data-ttu-id="b402a-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="b402a-109">S_OK</span></span> 
  
> <span data-ttu-id="b402a-110">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b402a-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b402a-111">����</span><span class="sxs-lookup"><span data-stu-id="b402a-111">Remarks</span></span>

<span data-ttu-id="b402a-112">フォームは、メッセージを保存することを要求する**IMAPIMessageSite::SaveMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b402a-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="b402a-113">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b402a-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b402a-114">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b402a-114">MFCMAPI reference</span></span>

<span data-ttu-id="b402a-115">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b402a-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b402a-116">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b402a-116">**File**</span></span>|<span data-ttu-id="b402a-117">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b402a-117">**Function**</span></span>|<span data-ttu-id="b402a-118">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b402a-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b402a-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b402a-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b402a-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="b402a-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="b402a-121">MFCMAPI では、 **IMAPIMessageSite::SaveMessage**メソッドを使用してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="b402a-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b402a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b402a-122">See also</span></span>



[<span data-ttu-id="b402a-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b402a-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="b402a-124">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b402a-124">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b402a-125">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b402a-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

