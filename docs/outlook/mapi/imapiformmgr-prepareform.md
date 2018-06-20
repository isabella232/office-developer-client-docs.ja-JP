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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800572"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="31363-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="31363-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="31363-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31363-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31363-105">開始するためのフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="31363-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="31363-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="31363-106">Parameters</span></span>

 <span data-ttu-id="31363-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="31363-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="31363-108">[in]フォームをダウンロード中に表示される進行状況のインジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="31363-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="31363-109">_UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="31363-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="31363-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31363-110">_ulFlags_</span></span>
  
> <span data-ttu-id="31363-111">[in]フォームをダウンロードする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="31363-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="31363-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="31363-112">The following flag can be set:</span></span>
    
<span data-ttu-id="31363-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="31363-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="31363-114">ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。</span><span class="sxs-lookup"><span data-stu-id="31363-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="31363-115">このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="31363-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="31363-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="31363-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="31363-117">[in]ダウンロードするフォームのフォームについてはオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="31363-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31363-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="31363-118">Return value</span></span>

<span data-ttu-id="31363-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="31363-119">S_OK</span></span> 
  
> <span data-ttu-id="31363-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="31363-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31363-121">����</span><span class="sxs-lookup"><span data-stu-id="31363-121">Remarks</span></span>

<span data-ttu-id="31363-122">フォーム ビューアーでは、開くフォームのコンテナーからフォームをダウンロードする**IMAPIFormMgr::PrepareForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31363-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="31363-123">フォームのほとんどのビューアーは、 [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)と[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)の両方のメソッドが必要な場合は、 **PrepareForm**を呼び出すため**PrepareForm**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="31363-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="31363-124">ダイナミック リンク ライブラリ (Dll) とそれらを変更するのにはフォームに関連付けられているその他のファイルを取得するのに**PrepareForm**を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="31363-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="31363-125">変更後のフォームは、フォームのコンテナーに読み込まれている場合に再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31363-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31363-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="31363-126">See also</span></span>



[<span data-ttu-id="31363-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="31363-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="31363-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="31363-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="31363-129">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="31363-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

