---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405087"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="05ac0-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="05ac0-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="05ac0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05ac0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05ac0-105">フォームライブラリにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="05ac0-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="05ac0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="05ac0-106">Parameters</span></span>

 <span data-ttu-id="05ac0-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="05ac0-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="05ac0-108">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="05ac0-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="05ac0-109">_uluiparam_パラメーターは、クライアントアプリケーションが_ulflags_パラメーターに MAPI_DIALOG フラグを設定していない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="05ac0-110">_uluiparam_パラメーターは、MAPI_DIALOG も渡されない場合は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="05ac0-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05ac0-111">_ulFlags_</span></span>
  
> <span data-ttu-id="05ac0-112">順番フォームのインストールを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="05ac0-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="05ac0-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-113">The following flags can be set:</span></span>
    
<span data-ttu-id="05ac0-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="05ac0-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="05ac0-115">進捗状況の情報を提供するダイアログボックスを表示します。詳細については、ユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="05ac0-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="05ac0-116">このフラグが設定されていない場合は、ダイアログボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="05ac0-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="05ac0-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05ac0-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="05ac0-118">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="05ac0-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="05ac0-119">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="05ac0-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="05ac0-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="05ac0-121">このフォームによって処理されるメッセージクラスを処理する別のフォームが既に存在する場合は、既存のフォームをこのフォームに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="05ac0-122">MAPI_DIALOG フラグも指定されている場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="05ac0-123">_szcfgpathname_</span><span class="sxs-lookup"><span data-stu-id="05ac0-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="05ac0-124">順番フォームの構成ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="05ac0-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05ac0-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="05ac0-125">Return value</span></span>

<span data-ttu-id="05ac0-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="05ac0-126">S_OK</span></span> 
  
> <span data-ttu-id="05ac0-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="05ac0-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="05ac0-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="05ac0-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="05ac0-129">実装エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="05ac0-129">An implementation error occurred.</span></span> <span data-ttu-id="05ac0-130">エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [imapiformcontainer:: GetLastError](imapiformcontainer-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="05ac0-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="05ac0-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="05ac0-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="05ac0-132">ユーザーがフォームのインストールをキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="05ac0-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="05ac0-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="05ac0-133">Notes to implementers</span></span>

<span data-ttu-id="05ac0-134">フォームライブラリプロバイダーは、次のいずれかの状況が発生した場合に、 **MAPIERROR**構造に記入し、MAPI_E_EXTENDED_ERROR を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="05ac0-135">構成ファイルが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="05ac0-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="05ac0-136">構成ファイルは読み取ることができません。</span><span class="sxs-lookup"><span data-stu-id="05ac0-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="05ac0-137">構成ファイルが無効です。</span><span class="sxs-lookup"><span data-stu-id="05ac0-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="05ac0-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="05ac0-138">Notes to callers</span></span>

<span data-ttu-id="05ac0-139">クライアントアプリケーションは、 **imapiformcontainer:: installform**メソッドを呼び出して、特定のフォームコンテナーにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="05ac0-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="05ac0-140">_szcfgpathname_パラメーターには、フォーム構成ファイル (つまり、フォームとその実装を記述する拡張子が付いたファイル) のパスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="05ac0-141">_ulflags_パラメーターのフラグには、次のものを指定します。</span><span class="sxs-lookup"><span data-stu-id="05ac0-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="05ac0-142">MAPI_DIALOG フラグが設定されている場合は、ユーザーインターフェイスが表示され、フォームをインストールしているユーザーがインストールの詳細を指定できます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="05ac0-143">MAPIFORM_INSTALL_OVERWRITEONCONFLICT フラグが設定されている場合、同じメッセージクラスの以前のフォームは、インストールされているフォームに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="05ac0-144">それ以外の場合は、フォームのインストールは現在のフォームの説明に結合されます (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="05ac0-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="05ac0-145">MAPI_DIALOG が設定されている場合、MAPIFORM_INSTALL_OVERWRITEONCONFLICT は無視されます。</span><span class="sxs-lookup"><span data-stu-id="05ac0-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="05ac0-146">フラグセットに MAPIFORM_INSTALL_OVERWRITEONCONFLICT がない場合は、マージが行われることを意味します。</span><span class="sxs-lookup"><span data-stu-id="05ac0-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="05ac0-147">現在フォームの説明に表示されていない、cfg ファイルの新しいプラットフォームがインストールされ、その他の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="05ac0-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="05ac0-148">MAPI_UNICODE フラグが設定されている場合、フォーム構成ファイルのパスは UNICODE 文字列になります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="05ac0-149">クライアントは[imapiformcontainer:: GetLastError](imapiformcontainer-getlasterror.md)を呼び出し\*\*\*\* て MAPI_E_EXTENDED_ERROR を返す必要があり、返された[MAPIERROR](mapierror.md)構造を調べて、エラーが発生した条件を特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05ac0-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="05ac0-150">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="05ac0-150">MFCMAPI reference</span></span>

<span data-ttu-id="05ac0-151">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05ac0-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05ac0-152">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="05ac0-152">**File**</span></span>|<span data-ttu-id="05ac0-153">**関数**</span><span class="sxs-lookup"><span data-stu-id="05ac0-153">**Function**</span></span>|<span data-ttu-id="05ac0-154">**コメント**</span><span class="sxs-lookup"><span data-stu-id="05ac0-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05ac0-155">FormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="05ac0-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="05ac0-156">CFormContainerDlg:: oninstallform</span><span class="sxs-lookup"><span data-stu-id="05ac0-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="05ac0-157">mfcmapi は、 **imapiformcontainer:: installform**メソッドを使用してフォームコンテナーにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="05ac0-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05ac0-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="05ac0-158">See also</span></span>



[<span data-ttu-id="05ac0-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="05ac0-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="05ac0-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05ac0-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="05ac0-161">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="05ac0-161">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

