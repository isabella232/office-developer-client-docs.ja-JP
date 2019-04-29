---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428593"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="bae73-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="bae73-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="bae73-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bae73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bae73-105">ユーザーがフォームコンテナーを選択できるようにするダイアログボックスを提供し、ユーザーが選択したコンテナーオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="bae73-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="bae73-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bae73-106">Parameters</span></span>

 <span data-ttu-id="bae73-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="bae73-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="bae73-108">順番表示されるダイアログボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="bae73-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="bae73-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bae73-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bae73-110">順番フォームライブラリの選択方法 (つまり、フォームコンテナーの選択方法) を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bae73-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="bae73-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bae73-111">The following flags can be set:</span></span>
    
<span data-ttu-id="bae73-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="bae73-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="bae73-113">選択は、すべてのコンテナーから行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bae73-113">Selection can be made from all containers.</span></span> <span data-ttu-id="bae73-114">これは既定の選択の種類です。</span><span class="sxs-lookup"><span data-stu-id="bae73-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="bae73-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="bae73-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="bae73-116">選択は、フォルダーコンテナーからのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bae73-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="bae73-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="bae73-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="bae73-118">選択は、フォルダーに関連付けられていないコンテナーからのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bae73-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="bae73-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="bae73-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="bae73-120">読み上げ返されるインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bae73-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="bae73-121">このインターフェイスは、ユーザーによって選択された container オブジェクトに対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="bae73-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bae73-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="bae73-122">Return value</span></span>

<span data-ttu-id="bae73-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="bae73-123">S_OK</span></span> 
  
> <span data-ttu-id="bae73-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bae73-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bae73-125">注釈</span><span class="sxs-lookup"><span data-stu-id="bae73-125">Remarks</span></span>

<span data-ttu-id="bae73-126">通常、フォームビューアーは、 **imapiformmgr:: selectformcontainer**メソッドを呼び出して、フォームがインストールされているフォームコンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="bae73-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="bae73-127">**selectformcontainer**を使用してローカルフォームコンテナーを選択することはできません。これは、値が HFRMREG_LOCAL です。</span><span class="sxs-lookup"><span data-stu-id="bae73-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bae73-128">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="bae73-128">MFCMAPI reference</span></span>

<span data-ttu-id="bae73-129">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bae73-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bae73-130">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="bae73-130">**File**</span></span>|<span data-ttu-id="bae73-131">**関数**</span><span class="sxs-lookup"><span data-stu-id="bae73-131">**Function**</span></span>|<span data-ttu-id="bae73-132">**コメント**</span><span class="sxs-lookup"><span data-stu-id="bae73-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bae73-133">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="bae73-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="bae73-134">CMainDlg:: onselectformcontainer</span><span class="sxs-lookup"><span data-stu-id="bae73-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="bae73-135">mfcmapi は、 **imapiformmgr:: selectformcontainer**メソッドを使用して、コンテンツをレンダリングする前にフォームコンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="bae73-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bae73-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="bae73-136">See also</span></span>



[<span data-ttu-id="bae73-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bae73-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="bae73-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bae73-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

