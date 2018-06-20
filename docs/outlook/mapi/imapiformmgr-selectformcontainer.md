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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800591"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="95051-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="95051-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="95051-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95051-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95051-105">により、ユーザーがフォームのコンテナーを選択し、ユーザーが選択したコンテナーのオブジェクトのインターフェイスを返しますダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95051-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="95051-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="95051-106">Parameters</span></span>

 <span data-ttu-id="95051-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="95051-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="95051-108">[in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="95051-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="95051-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95051-109">_ulFlags_</span></span>
  
> <span data-ttu-id="95051-110">[in]フォーム ライブラリを選択する方法を制御するフラグのビットマスク (どのようにフォームのコンテナーがオンになっている)。</span><span class="sxs-lookup"><span data-stu-id="95051-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="95051-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="95051-111">The following flags can be set:</span></span>
    
<span data-ttu-id="95051-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="95051-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="95051-113">すべてのコンテナーの選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="95051-113">Selection can be made from all containers.</span></span> <span data-ttu-id="95051-114">これは、既定の選択の種類です。</span><span class="sxs-lookup"><span data-stu-id="95051-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="95051-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="95051-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="95051-116">フォルダー コンテナーからのみ選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="95051-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="95051-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="95051-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="95051-118">いないフォルダーに関連付けられているコンテナーからのみ選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="95051-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="95051-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="95051-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="95051-120">[out]返されたインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95051-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="95051-121">インターフェイスは、ユーザーが選択されているコンテナー オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="95051-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95051-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="95051-122">Return value</span></span>

<span data-ttu-id="95051-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="95051-123">S_OK</span></span> 
  
> <span data-ttu-id="95051-124">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="95051-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95051-125">����</span><span class="sxs-lookup"><span data-stu-id="95051-125">Remarks</span></span>

<span data-ttu-id="95051-126">フォーム ビューアーは、通常、フォームがインストールされているフォームのコンテナーを選択する**IMAPIFormMgr::SelectFormContainer**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="95051-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="95051-127">**SelectFormContainer**は、HFRMREG_LOCAL の値を持つローカルのフォームのコンテナーを選択するのには使用できません。</span><span class="sxs-lookup"><span data-stu-id="95051-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="95051-128">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="95051-128">MFCMAPI reference</span></span>

<span data-ttu-id="95051-129">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="95051-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="95051-130">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="95051-130">**File**</span></span>|<span data-ttu-id="95051-131">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="95051-131">**Function**</span></span>|<span data-ttu-id="95051-132">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="95051-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95051-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="95051-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="95051-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="95051-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="95051-135">MFCMAPI では、 **IMAPIFormMgr::SelectFormContainer**メソッドを使用して、その内容をレンダリングする前にフォームのコンテナーを選択します。</span><span class="sxs-lookup"><span data-stu-id="95051-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95051-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="95051-136">See also</span></span>



[<span data-ttu-id="95051-137">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="95051-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


<span data-ttu-id="95051-138">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="95051-138">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

