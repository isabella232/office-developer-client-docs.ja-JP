---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416651"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="b1ac3-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="b1ac3-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="b1ac3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1ac3-105">開くフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="b1ac3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1ac3-106">Parameters</span></span>

 <span data-ttu-id="b1ac3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b1ac3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b1ac3-108">[in]フォームのダウンロード中に表示される進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="b1ac3-109">_ulUIParam_ パラメーターは _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b1ac3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1ac3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b1ac3-111">[in]フォームのダウンロード方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="b1ac3-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b1ac3-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b1ac3-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b1ac3-114">ユーザー インターフェイスを表示して、状態を提供するか、ユーザーに詳細を求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="b1ac3-115">このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="b1ac3-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="b1ac3-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="b1ac3-117">[in]ダウンロードするフォームのフォーム情報オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1ac3-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="b1ac3-118">Return value</span></span>

<span data-ttu-id="b1ac3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1ac3-119">S_OK</span></span> 
  
> <span data-ttu-id="b1ac3-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b1ac3-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1ac3-121">注釈</span><span class="sxs-lookup"><span data-stu-id="b1ac3-121">Remarks</span></span>

<span data-ttu-id="b1ac3-122">フォーム ビューアーは **IMAPIFormMgr::P repareForm** メソッドを呼び出して、開くフォーム コンテナーからフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="b1ac3-123">[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)メソッドと [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)メソッドの両方が必要に応じて **PrepareForm** を呼び出すので、ほとんどのフォーム ビューアーは **PrepareForm** を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="b1ac3-124">**PrepareForm を使用して**、フォームに関連付けられた動的リンク ライブラリ (DLL) および他のファイルを取得して、それらを変更できます。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="b1ac3-125">変更されたフォームがフォーム コンテナーに読み込まれた場合は、再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ac3-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1ac3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1ac3-126">See also</span></span>



[<span data-ttu-id="b1ac3-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="b1ac3-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="b1ac3-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="b1ac3-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="b1ac3-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1ac3-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

