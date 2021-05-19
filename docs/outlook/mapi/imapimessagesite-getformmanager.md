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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419458"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="b3650-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="b3650-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="b3650-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3650-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3650-105">フォーム サーバーが別のフォーム サーバーを開くのに使用できるフォーム マネージャー インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="b3650-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="b3650-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3650-106">Parameters</span></span>

 <span data-ttu-id="b3650-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="b3650-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="b3650-108">[out]返されるフォーム マネージャー インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b3650-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3650-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="b3650-109">Return value</span></span>

<span data-ttu-id="b3650-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3650-110">S_OK</span></span> 
  
> <span data-ttu-id="b3650-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b3650-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3650-112">注釈</span><span class="sxs-lookup"><span data-stu-id="b3650-112">Remarks</span></span>

<span data-ttu-id="b3650-113">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="b3650-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b3650-114">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b3650-114">MFCMAPI reference</span></span>

<span data-ttu-id="b3650-115">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3650-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b3650-116">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b3650-116">**File**</span></span>|<span data-ttu-id="b3650-117">**関数**</span><span class="sxs-lookup"><span data-stu-id="b3650-117">**Function**</span></span>|<span data-ttu-id="b3650-118">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b3650-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b3650-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b3650-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b3650-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="b3650-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="b3650-121">MFCMAPI は **IMAPIMessageSite::GetFormManager** メソッドを使用して [MAPIOpenFormMgr](mapiopenformmgr.md) を呼び出し、その呼び出しの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="b3650-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3650-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3650-122">See also</span></span>



[<span data-ttu-id="b3650-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="b3650-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="b3650-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3650-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="b3650-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b3650-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b3650-126">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b3650-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

