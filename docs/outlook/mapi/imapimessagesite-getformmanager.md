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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800602"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="23cb8-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="23cb8-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="23cb8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23cb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23cb8-105">フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="23cb8-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="23cb8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="23cb8-106">Parameters</span></span>

 <span data-ttu-id="23cb8-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="23cb8-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="23cb8-108">[out]返されるフォーム マネージャーのインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="23cb8-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23cb8-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="23cb8-109">Return value</span></span>

<span data-ttu-id="23cb8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="23cb8-110">S_OK</span></span> 
  
> <span data-ttu-id="23cb8-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="23cb8-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23cb8-112">����</span><span class="sxs-lookup"><span data-stu-id="23cb8-112">Remarks</span></span>

<span data-ttu-id="23cb8-113">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23cb8-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="23cb8-114">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="23cb8-114">MFCMAPI reference</span></span>

<span data-ttu-id="23cb8-115">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="23cb8-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="23cb8-116">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="23cb8-116">**File**</span></span>|<span data-ttu-id="23cb8-117">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="23cb8-117">**Function**</span></span>|<span data-ttu-id="23cb8-118">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="23cb8-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23cb8-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="23cb8-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="23cb8-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="23cb8-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="23cb8-121">MFCMAPI では、 **IMAPIMessageSite::GetFormManager**メソッドを使用して、 [MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出すし、その呼び出しの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="23cb8-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23cb8-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="23cb8-122">See also</span></span>



[<span data-ttu-id="23cb8-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="23cb8-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="23cb8-124">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="23cb8-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="23cb8-125">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="23cb8-125">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="23cb8-126">MAPI フォームのインタ フェース</span><span class="sxs-lookup"><span data-stu-id="23cb8-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

