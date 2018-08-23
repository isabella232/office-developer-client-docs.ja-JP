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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577927"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="59e0c-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="59e0c-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="59e0c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59e0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59e0c-105">により、ユーザーがフォームのコンテナーを選択し、ユーザーが選択したコンテナーのオブジェクトのインターフェイスを返しますダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59e0c-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="59e0c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59e0c-106">Parameters</span></span>

 <span data-ttu-id="59e0c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="59e0c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="59e0c-108">[in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="59e0c-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="59e0c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59e0c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="59e0c-110">[in]フォーム ライブラリを選択する方法を制御するフラグのビットマスク (どのようにフォームのコンテナーがオンになっている)。</span><span class="sxs-lookup"><span data-stu-id="59e0c-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="59e0c-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="59e0c-111">The following flags can be set:</span></span>
    
<span data-ttu-id="59e0c-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="59e0c-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="59e0c-113">すべてのコンテナーの選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="59e0c-113">Selection can be made from all containers.</span></span> <span data-ttu-id="59e0c-114">これは、既定の選択の種類です。</span><span class="sxs-lookup"><span data-stu-id="59e0c-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="59e0c-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="59e0c-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="59e0c-116">フォルダー コンテナーからのみ選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="59e0c-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="59e0c-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="59e0c-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="59e0c-118">いないフォルダーに関連付けられているコンテナーからのみ選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="59e0c-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="59e0c-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="59e0c-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="59e0c-120">[out]返されたインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="59e0c-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="59e0c-121">インターフェイスは、ユーザーが選択されているコンテナー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="59e0c-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59e0c-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="59e0c-122">Return value</span></span>

<span data-ttu-id="59e0c-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="59e0c-123">S_OK</span></span> 
  
> <span data-ttu-id="59e0c-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="59e0c-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59e0c-125">����</span><span class="sxs-lookup"><span data-stu-id="59e0c-125">Remarks</span></span>

<span data-ttu-id="59e0c-126">フォーム ビューアーは、通常、フォームがインストールされているフォームのコンテナーを選択する**IMAPIFormMgr::SelectFormContainer**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="59e0c-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="59e0c-127">**SelectFormContainer**は、HFRMREG_LOCAL の値を持つローカルのフォームのコンテナーを選択するのには使用できません。</span><span class="sxs-lookup"><span data-stu-id="59e0c-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="59e0c-128">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="59e0c-128">MFCMAPI reference</span></span>

<span data-ttu-id="59e0c-129">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="59e0c-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="59e0c-130">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="59e0c-130">**File**</span></span>|<span data-ttu-id="59e0c-131">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="59e0c-131">**Function**</span></span>|<span data-ttu-id="59e0c-132">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="59e0c-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59e0c-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="59e0c-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="59e0c-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="59e0c-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="59e0c-135">MFCMAPI では、 **IMAPIFormMgr::SelectFormContainer**メソッドを使用して、その内容をレンダリングする前にフォームのコンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="59e0c-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59e0c-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="59e0c-136">See also</span></span>



[<span data-ttu-id="59e0c-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59e0c-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="59e0c-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="59e0c-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

