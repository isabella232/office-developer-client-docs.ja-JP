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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d329d3a14b6026d0bd62df9feba6ccff251e4151
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800524"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="eacc7-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="eacc7-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="eacc7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eacc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eacc7-105">フォーム ライブラリにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="eacc7-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="eacc7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eacc7-106">Parameters</span></span>

 <span data-ttu-id="eacc7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="eacc7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="eacc7-108">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="eacc7-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="eacc7-109">_UlUIParam_パラメーターは、クライアント アプリケーションは、 _ulFlags_パラメーターで MAPI_DIALOG フラグを設定しない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="eacc7-110">MAPI_DIALOG が渡されてもいない場合は、 _ulUIParam_パラメーターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="eacc7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eacc7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="eacc7-112">[in]フォームのインストールを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="eacc7-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="eacc7-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-113">The following flags can be set:</span></span>
    
<span data-ttu-id="eacc7-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="eacc7-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="eacc7-115">進行状況情報を提供したり、詳細情報をユーザーに確認するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="eacc7-116">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="eacc7-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="eacc7-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eacc7-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eacc7-118">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="eacc7-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="eacc7-119">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="eacc7-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="eacc7-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="eacc7-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="eacc7-121">別のフォームによって、メッセージ クラスは、このフォームで処理するハンドルが既に存在する場合は、既存のフォームをこれと置き換えます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="eacc7-122">MAPI_DIALOG フラグが存在しても場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="eacc7-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="eacc7-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="eacc7-124">[in]フォームの構成ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="eacc7-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eacc7-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="eacc7-125">Return value</span></span>

<span data-ttu-id="eacc7-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="eacc7-126">S_OK</span></span> 
  
> <span data-ttu-id="eacc7-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="eacc7-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eacc7-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="eacc7-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="eacc7-129">実装エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="eacc7-129">An implementation error occurred.</span></span> <span data-ttu-id="eacc7-130">エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eacc7-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="eacc7-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="eacc7-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="eacc7-132">ユーザー] ダイアログ ボックスで [**キャンセル**] ボタンをクリックすると、通常、フォームのインストールをキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="eacc7-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="eacc7-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="eacc7-133">Notes to implementers</span></span>

<span data-ttu-id="eacc7-134">フォーム ライブラリのプロバイダーは、 **MAPIERROR**構造体を入力し、次の条件のいずれかが発生した場合は、MAPI_E_EXTENDED_ERROR を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eacc7-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="eacc7-135">構成ファイルが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="eacc7-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="eacc7-136">構成ファイルを読み取ることができません。</span><span class="sxs-lookup"><span data-stu-id="eacc7-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="eacc7-137">構成ファイルが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="eacc7-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="eacc7-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="eacc7-138">Notes to callers</span></span>

<span data-ttu-id="eacc7-139">クライアント アプリケーションは、フォームをフォームの特定のコンテナーにインストールするのには**IMAPIFormContainer::InstallForm**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eacc7-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="eacc7-140">_SzCfgPathName_パラメーターには、フォーム構成ファイル (つまり、フォームとその実装を記述する .cfg ファイルの拡張子を持つファイルの場合) のパスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eacc7-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="eacc7-141">_UlFlags_パラメーター内のフラグは、以下のいずれかを指定します。</span><span class="sxs-lookup"><span data-stu-id="eacc7-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="eacc7-142">MAPI_DIALOG フラグが設定されている場合は、ユーザー インターフェイスが表示されます、インストールの詳細を指定するフォームをインストールしているユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="eacc7-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="eacc7-143">MAPIFORM_INSTALL_OVERWRITEONCONFLICT フラグが設定されている場合は、同じメッセージ クラスのすべての前のフォームがインストールされているフォームに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="eacc7-144">それ以外の場合、フォームのインストールは、存在する場合、現在のフォームの説明に統合されます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="eacc7-145">MAPI_DIALOG が設定されている場合は、MAPIFORM_INSTALL_OVERWRITEONCONFLICT は無視されます。</span><span class="sxs-lookup"><span data-stu-id="eacc7-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="eacc7-146">MAPIFORM_INSTALL_OVERWRITEONCONFLICT のフラグでない場合は、差し込み印刷が行われることを意味を設定します。</span><span class="sxs-lookup"><span data-stu-id="eacc7-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="eacc7-147">.Cfg ファイルの現在のフォームの説明ではない新しいプラットフォームをインストールして、その他の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="eacc7-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="eacc7-148">フォーム構成ファイルのパスは、MAPI_UNICODE フラグが設定されている場合は、Unicode 文字列になります。</span><span class="sxs-lookup"><span data-stu-id="eacc7-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="eacc7-149">**InstallForm**は、MAPI_E_EXTENDED_ERROR を返し、エラーが発生した状態を判断するのには返された[MAPIERROR](mapierror.md)構造体をチェックする必要がある場合、クライアントは[IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eacc7-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eacc7-150">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="eacc7-150">MFCMAPI reference</span></span>

<span data-ttu-id="eacc7-151">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="eacc7-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eacc7-152">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="eacc7-152">**File**</span></span>|<span data-ttu-id="eacc7-153">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="eacc7-153">**Function**</span></span>|<span data-ttu-id="eacc7-154">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="eacc7-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eacc7-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="eacc7-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="eacc7-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="eacc7-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="eacc7-157">MFCMAPI では、 **IMAPIFormContainer::InstallForm**メソッドを使用して、フォームのコンテナー内のフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="eacc7-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eacc7-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="eacc7-158">See also</span></span>



[<span data-ttu-id="eacc7-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="eacc7-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="eacc7-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eacc7-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="eacc7-161">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="eacc7-161">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

