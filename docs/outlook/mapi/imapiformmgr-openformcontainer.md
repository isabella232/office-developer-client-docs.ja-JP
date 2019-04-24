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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321638"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="81775-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="81775-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="81775-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81775-105">特定のフォームコンテナーの[imapiformcontainer](imapiformcontaineriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="81775-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="81775-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81775-106">Parameters</span></span>

 <span data-ttu-id="81775-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="81775-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="81775-108">順番開く (つまり、開くフォームコンテナーである) フォームライブラリを示す hfrmreg 列挙。</span><span class="sxs-lookup"><span data-stu-id="81775-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="81775-109">hfrmreg 列挙は、フォームライブラリプロバイダーに固有の列挙型です。</span><span class="sxs-lookup"><span data-stu-id="81775-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="81775-110">可能な hfrmreg 値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="81775-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="81775-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="81775-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="81775-112">便利なフォームコンテナー。</span><span class="sxs-lookup"><span data-stu-id="81775-112">A convenient form container.</span></span>
    
<span data-ttu-id="81775-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="81775-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="81775-114">フォルダーコンテナー。</span><span class="sxs-lookup"><span data-stu-id="81775-114">A folder container.</span></span> 
    
<span data-ttu-id="81775-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="81775-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="81775-116">既定のメッセージストアのコンテナー。</span><span class="sxs-lookup"><span data-stu-id="81775-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="81775-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="81775-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="81775-118">ローカルフォームコンテナー。</span><span class="sxs-lookup"><span data-stu-id="81775-118">A local form container.</span></span> 
    
 <span data-ttu-id="81775-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="81775-119">_lpunk_</span></span>
  
> <span data-ttu-id="81775-120">順番インターフェイスを開くオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="81775-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="81775-121">_hfrmreg_パラメーターの値にオブジェクトポインターが必要でない場合は、 _lpunk_パラメーターを**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81775-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="81775-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="81775-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="81775-123">読み上げ返される form container オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="81775-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81775-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="81775-124">Return value</span></span>

<span data-ttu-id="81775-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="81775-125">S_OK</span></span> 
  
> <span data-ttu-id="81775-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="81775-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="81775-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="81775-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="81775-128">_lpunk_が指すオブジェクトは、必要なインターフェイスをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="81775-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81775-129">解説</span><span class="sxs-lookup"><span data-stu-id="81775-129">Remarks</span></span>

<span data-ttu-id="81775-130">フォームビューアーは、 **imapiformmgr:: openformcontainer**メソッドを呼び出して、特定のフォームコンテナーの**imapiformmgr**インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="81775-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="81775-131">このインターフェイスは、フォームをフォームコンテナーにインストールしたり、フォームを削除したりするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="81775-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="81775-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="81775-132">Notes to callers</span></span>

<span data-ttu-id="81775-133">_hfrmreg_の値が HFRMREG_FOLDER の場合、 _lpunk_で使用されるインターフェイス識別子は**null**以外の値である必要があります。また、 [imapifolder](imapifolderimapicontainer.md)インターフェイスに対する[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの呼び出しを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81775-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="81775-134">ローカルフォームコンテナーを開くには、 **openformcontainer**メソッドまたは[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数への呼び出しを使用する必要があります。[imapiformmgr:: selectformcontainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、ユーザーがローカルフォームコンテナーを選択できるようにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="81775-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81775-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="81775-135">MFCMAPI reference</span></span>

<span data-ttu-id="81775-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81775-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81775-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="81775-137">**File**</span></span>|<span data-ttu-id="81775-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="81775-138">**Function**</span></span>|<span data-ttu-id="81775-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="81775-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81775-140">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="81775-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="81775-141">CMainDlg:: onopenformcontainer</span><span class="sxs-lookup"><span data-stu-id="81775-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="81775-142">mfcmapi は、 **imapiformmgr:: openformcontainer**メソッドを使用して、コンテナーの内容を表示できるようにフォームコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="81775-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="81775-143">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="81775-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="81775-144">CMsgStoreDlg:: onopenformcontainer</span><span class="sxs-lookup"><span data-stu-id="81775-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="81775-145">mfcmapi は、 **imapiformmgr:: openformcontainer**メソッドを使用して、コンテナーの内容を表示できるようにフォルダーのフォームコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="81775-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81775-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="81775-146">See also</span></span>



[<span data-ttu-id="81775-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="81775-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="81775-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="81775-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="81775-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="81775-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="81775-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81775-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="81775-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="81775-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

