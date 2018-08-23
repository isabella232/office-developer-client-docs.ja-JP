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
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570493"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="b609a-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="b609a-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="b609a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b609a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b609a-105">フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="b609a-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="b609a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b609a-106">Parameters</span></span>

 <span data-ttu-id="b609a-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="b609a-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="b609a-108">[out]返されるフォーム マネージャーのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b609a-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b609a-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b609a-109">Return value</span></span>

<span data-ttu-id="b609a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b609a-110">S_OK</span></span> 
  
> <span data-ttu-id="b609a-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b609a-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b609a-112">����</span><span class="sxs-lookup"><span data-stu-id="b609a-112">Remarks</span></span>

<span data-ttu-id="b609a-113">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b609a-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b609a-114">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b609a-114">MFCMAPI reference</span></span>

<span data-ttu-id="b609a-115">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b609a-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b609a-116">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b609a-116">**File**</span></span>|<span data-ttu-id="b609a-117">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b609a-117">**Function**</span></span>|<span data-ttu-id="b609a-118">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b609a-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b609a-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b609a-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b609a-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="b609a-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="b609a-121">MFCMAPI では、 **IMAPIMessageSite::GetFormManager**メソッドを使用して、 [MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出すし、その呼び出しの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="b609a-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b609a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b609a-122">See also</span></span>



[<span data-ttu-id="b609a-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="b609a-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="b609a-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b609a-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="b609a-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b609a-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="b609a-126">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b609a-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

