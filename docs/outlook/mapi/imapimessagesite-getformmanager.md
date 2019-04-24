---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321373"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="e1aaa-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="e1aaa-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="e1aaa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1aaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1aaa-105">フォームサーバーが別のフォームサーバーを開くために使用できるフォームマネージャーインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="e1aaa-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="e1aaa-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1aaa-106">Parameters</span></span>

 <span data-ttu-id="e1aaa-107">_ppformmgr_</span><span class="sxs-lookup"><span data-stu-id="e1aaa-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="e1aaa-108">読み上げ返されるフォームマネージャーインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e1aaa-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1aaa-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e1aaa-109">Return value</span></span>

<span data-ttu-id="e1aaa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1aaa-110">S_OK</span></span> 
  
> <span data-ttu-id="e1aaa-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e1aaa-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1aaa-112">解説</span><span class="sxs-lookup"><span data-stu-id="e1aaa-112">Remarks</span></span>

<span data-ttu-id="e1aaa-113">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1aaa-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1aaa-114">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e1aaa-114">MFCMAPI reference</span></span>

<span data-ttu-id="e1aaa-115">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1aaa-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1aaa-116">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e1aaa-116">**File**</span></span>|<span data-ttu-id="e1aaa-117">**関数**</span><span class="sxs-lookup"><span data-stu-id="e1aaa-117">**Function**</span></span>|<span data-ttu-id="e1aaa-118">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e1aaa-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1aaa-119">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="e1aaa-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="e1aaa-120">cmymapiformviewer:: getformmanager</span><span class="sxs-lookup"><span data-stu-id="e1aaa-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="e1aaa-121">mfcmapi は、 **IMAPIMessageSite:: getformmanager**メソッドを使用して[MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出し、その呼び出しの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="e1aaa-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1aaa-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1aaa-122">See also</span></span>



[<span data-ttu-id="e1aaa-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="e1aaa-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="e1aaa-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1aaa-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="e1aaa-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e1aaa-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="e1aaa-126">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e1aaa-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

