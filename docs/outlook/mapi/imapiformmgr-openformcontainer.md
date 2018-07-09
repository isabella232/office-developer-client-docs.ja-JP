---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 64031725e06a949464e7bfabb0a2f114d325470e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800559"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="98ddf-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="98ddf-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="98ddf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98ddf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98ddf-105">[IMAPIFormContainer](imapiformcontaineriunknown.md)インターフェイスの特定のフォームのコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="98ddf-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="98ddf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="98ddf-106">Parameters</span></span>

 <span data-ttu-id="98ddf-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="98ddf-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="98ddf-108">[in]開くにはフォーム ライブラリを示す HFRMREG 列挙型 (つまり、フォームはコンテナーを開くには)。</span><span class="sxs-lookup"><span data-stu-id="98ddf-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="98ddf-109">HFRMREG 列挙体は、フォーム ライブラリのプロバイダーに固有の列挙体です。</span><span class="sxs-lookup"><span data-stu-id="98ddf-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="98ddf-110">使用可能な HFRMREG の値を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="98ddf-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="98ddf-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="98ddf-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="98ddf-112">フォームの便利なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="98ddf-112">A convenient form container.</span></span>
    
<span data-ttu-id="98ddf-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="98ddf-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="98ddf-114">フォルダーのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="98ddf-114">A folder container.</span></span> 
    
<span data-ttu-id="98ddf-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="98ddf-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="98ddf-116">既定のメッセージ ストアのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="98ddf-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="98ddf-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="98ddf-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="98ddf-118">ローカル フォームのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="98ddf-118">A local form container.</span></span> 
    
 <span data-ttu-id="98ddf-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="98ddf-119">_lpunk_</span></span>
  
> <span data-ttu-id="98ddf-120">[in]インタ フェースを開く対象のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98ddf-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="98ddf-121">_Hfrmreg_パラメーターの値がオブジェクト ポインターを必要としない限り、 _lpunk_パラメーターを**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98ddf-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="98ddf-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="98ddf-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="98ddf-123">[out]返されるフォームのコンテナー オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98ddf-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98ddf-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="98ddf-124">Return value</span></span>

<span data-ttu-id="98ddf-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="98ddf-125">S_OK</span></span> 
  
> <span data-ttu-id="98ddf-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="98ddf-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="98ddf-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="98ddf-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="98ddf-128">_Lpunk_が指すオブジェクトは、必要なインターフェイスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="98ddf-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98ddf-129">備考</span><span class="sxs-lookup"><span data-stu-id="98ddf-129">Remarks</span></span>

<span data-ttu-id="98ddf-130">フォーム ビューアーは、特定のフォームのコンテナーの**IMAPIFormContainer**インターフェイスを開くに**IMAPIFormMgr::OpenFormContainer**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98ddf-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="98ddf-131">このインターフェイスにインストールを実行するフォームとフォームのコンテナーから削除するフォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="98ddf-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98ddf-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="98ddf-132">Notes to callers</span></span>

<span data-ttu-id="98ddf-133">_Hfrmreg_の値が HFRMREG_FOLDER の場合は、 _lpunk_で使用されているインタ フェース識別子は非**null**である必要があり、 [IMAPIFolder](imapifolderimapicontainer.md)インタ フェースを[IUnknown::QueryInterface](http://msdn.microsoft.com/ja-jp/library/ms682521%28v=VS.85%29.aspx)メソッドの呼び出しを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98ddf-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](http://msdn.microsoft.com/ja-jp/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="98ddf-134">ローカル フォームのコンテナーを開くには、 **OpenFormContainer**メソッドまたは[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しを使用する必要があります。ローカル フォームのコンテナーを選択するのにユーザーを有効にするのには、 [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="98ddf-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="98ddf-135">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="98ddf-135">MFCMAPI reference</span></span>

<span data-ttu-id="98ddf-136">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="98ddf-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="98ddf-137">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="98ddf-137">**File**</span></span>|<span data-ttu-id="98ddf-138">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="98ddf-138">**Function**</span></span>|<span data-ttu-id="98ddf-139">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="98ddf-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="98ddf-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="98ddf-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="98ddf-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="98ddf-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="98ddf-142">MFCMAPI では、 **IMAPIFormMgr::OpenFormContainer**メソッドを使用して、コンテナーの内容を表示できるように、フォームのコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="98ddf-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="98ddf-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="98ddf-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="98ddf-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="98ddf-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="98ddf-145">MFCMAPI では、 **IMAPIFormMgr::OpenFormContainer**メソッドを使用して、コンテナーの内容を表示できるようにフォルダーのフォームのコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="98ddf-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98ddf-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="98ddf-146">See also</span></span>



[<span data-ttu-id="98ddf-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="98ddf-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="98ddf-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="98ddf-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="98ddf-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="98ddf-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="98ddf-150">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="98ddf-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="98ddf-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="98ddf-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

