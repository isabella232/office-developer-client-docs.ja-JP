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
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="59948-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="59948-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="59948-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59948-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59948-105">ユーザーがフォーム コンテナーを選択できるダイアログ ボックスを表示し、ユーザーが選択したコンテナー オブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="59948-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="59948-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59948-106">Parameters</span></span>

 <span data-ttu-id="59948-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="59948-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="59948-108">[in]表示されるダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="59948-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="59948-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59948-109">_ulFlags_</span></span>
  
> <span data-ttu-id="59948-110">[in]フォーム ライブラリの選択方法 (フォーム コンテナーの選択方法) を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="59948-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="59948-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="59948-111">The following flags can be set:</span></span>
    
<span data-ttu-id="59948-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="59948-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="59948-113">すべてのコンテナーから選択できます。</span><span class="sxs-lookup"><span data-stu-id="59948-113">Selection can be made from all containers.</span></span> <span data-ttu-id="59948-114">これは既定の選択の種類です。</span><span class="sxs-lookup"><span data-stu-id="59948-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="59948-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="59948-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="59948-116">フォルダー コンテナーからのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="59948-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="59948-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="59948-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="59948-118">フォルダーに関連付けされていないコンテナーからのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="59948-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="59948-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="59948-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="59948-120">[out]返されたインターフェイスへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="59948-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="59948-121">このインターフェイスは、ユーザーが選択したコンテナー オブジェクト用です。</span><span class="sxs-lookup"><span data-stu-id="59948-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59948-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="59948-122">Return value</span></span>

<span data-ttu-id="59948-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="59948-123">S_OK</span></span> 
  
> <span data-ttu-id="59948-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="59948-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59948-125">注釈</span><span class="sxs-lookup"><span data-stu-id="59948-125">Remarks</span></span>

<span data-ttu-id="59948-126">フォーム ビューアーは通常 **、IMAPIFormMgr::SelectFormContainer** メソッドを呼び出して、フォームがインストールされているフォーム コンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="59948-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="59948-127">**SelectFormContainer** を使用してローカル フォーム コンテナーを選択することはできません。このコンテナーの値はHFRMREG_LOCAL。</span><span class="sxs-lookup"><span data-stu-id="59948-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="59948-128">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="59948-128">MFCMAPI reference</span></span>

<span data-ttu-id="59948-129">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59948-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="59948-130">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="59948-130">**File**</span></span>|<span data-ttu-id="59948-131">**関数**</span><span class="sxs-lookup"><span data-stu-id="59948-131">**Function**</span></span>|<span data-ttu-id="59948-132">**コメント**</span><span class="sxs-lookup"><span data-stu-id="59948-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59948-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="59948-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="59948-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="59948-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="59948-135">MFCMAPI は **IMAPIFormMgr::SelectFormContainer** メソッドを使用して、コンテンツをレンダリングする前にフォーム コンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="59948-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59948-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="59948-136">See also</span></span>



[<span data-ttu-id="59948-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59948-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="59948-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="59948-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

