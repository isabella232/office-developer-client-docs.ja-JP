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
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="cb87c-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="cb87c-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="cb87c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb87c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb87c-105">フォーム ライブラリにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="cb87c-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="cb87c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cb87c-106">Parameters</span></span>

 <span data-ttu-id="cb87c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cb87c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="cb87c-108">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="cb87c-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="cb87c-109">_ulUIParam_ パラメーターは、クライアント アプリケーションが _ulFlags_ パラメーターに MAPI_DIALOGフラグを設定しない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="cb87c-110">_ulUIParam_ パラメーターは、パラメーターも渡MAPI_DIALOG NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="cb87c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cb87c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cb87c-112">[in]フォームのインストールを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cb87c-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="cb87c-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-113">The following flags can be set:</span></span>
    
<span data-ttu-id="cb87c-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cb87c-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="cb87c-115">ダイアログ ボックスを表示して、進行状況情報を提供するか、ユーザーに詳細を求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="cb87c-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="cb87c-116">このフラグが設定されていない場合、ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="cb87c-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="cb87c-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb87c-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cb87c-118">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="cb87c-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="cb87c-119">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="cb87c-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="cb87c-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="cb87c-121">このフォームで処理されるメッセージ クラスを処理する別のフォームが既に存在する場合は、既存のフォームをこのフォームに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="cb87c-122">このフラグは、MAPI_DIALOGが存在する場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="cb87c-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="cb87c-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="cb87c-124">[in]フォームの構成ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="cb87c-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cb87c-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="cb87c-125">Return value</span></span>

<span data-ttu-id="cb87c-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb87c-126">S_OK</span></span> 
  
> <span data-ttu-id="cb87c-127">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cb87c-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cb87c-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="cb87c-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="cb87c-129">実装エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="cb87c-129">An implementation error occurred.</span></span> <span data-ttu-id="cb87c-130">エラーに関連 [付けられている MAPIERROR](mapierror.md) 構造を取得するには [、IMAPIFormContainer::GetLastError メソッドを呼び出](imapiformcontainer-getlasterror.md) します。</span><span class="sxs-lookup"><span data-stu-id="cb87c-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="cb87c-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cb87c-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cb87c-132">ユーザーは、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックして、フォームのインストールをキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="cb87c-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="cb87c-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="cb87c-133">Notes to implementers</span></span>

<span data-ttu-id="cb87c-134">フォーム ライブラリ プロバイダーは **、MAPIERROR** 構造を入力し、次MAPI_E_EXTENDED_ERROR条件が発生した場合は、このプロパティを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="cb87c-135">構成ファイルが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="cb87c-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="cb87c-136">構成ファイルは読み取り可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="cb87c-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="cb87c-137">構成ファイルが無効です。</span><span class="sxs-lookup"><span data-stu-id="cb87c-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="cb87c-138">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cb87c-138">Notes to callers</span></span>

<span data-ttu-id="cb87c-139">クライアント アプリケーションは **IMAPIFormContainer::InstallForm** メソッドを呼び出して、フォームを特定のフォーム コンテナーにインストールします。</span><span class="sxs-lookup"><span data-stu-id="cb87c-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="cb87c-140">_szCfgPathName_ パラメーターには、フォーム構成ファイルのパス (つまり、フォームとその実装を記述する .cfg 拡張子を持つファイル) が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="cb87c-141">_ulFlags パラメーターのフラグ_ は、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb87c-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="cb87c-142">[MAPI_DIALOG] フラグが設定されている場合は、ユーザー インターフェイスが表示され、フォームをインストールするユーザーがインストールの詳細を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="cb87c-143">このフラグMAPIFORM_INSTALL_OVERWRITEONCONFLICT設定すると、同じメッセージ クラスの前のフォームがインストールされているフォームに置き換えられる。</span><span class="sxs-lookup"><span data-stu-id="cb87c-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="cb87c-144">それ以外の場合、フォームのインストールは、現在のフォームの説明 (存在する場合) と結合されます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="cb87c-145">このMAPI_DIALOG設定されている場合、MAPIFORM_INSTALL_OVERWRITEONCONFLICTは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="cb87c-146">フラグ セットにMAPIFORM_INSTALL_OVERWRITEONCONFLICTがない場合は、マージが行われます。</span><span class="sxs-lookup"><span data-stu-id="cb87c-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="cb87c-147">フォームの説明に現在存在しない .cfg ファイル内の新しいプラットフォームはインストールされ、その他の変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="cb87c-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="cb87c-148">このフラグMAPI_UNICODE設定すると、フォーム構成ファイルのパスは Unicode 文字列になります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="cb87c-149">InstallForm が MAPI_E_EXTENDED_ERROR を返す場合、クライアントは[IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)を呼び出す必要があります。エラーが発生した条件を判断するには、返された[MAPIERROR](mapierror.md)構造を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb87c-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cb87c-150">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cb87c-150">MFCMAPI reference</span></span>

<span data-ttu-id="cb87c-151">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb87c-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cb87c-152">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb87c-152">**File**</span></span>|<span data-ttu-id="cb87c-153">**関数**</span><span class="sxs-lookup"><span data-stu-id="cb87c-153">**Function**</span></span>|<span data-ttu-id="cb87c-154">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cb87c-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb87c-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cb87c-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="cb87c-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="cb87c-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="cb87c-157">MFCMAPI は **IMAPIFormContainer::InstallForm** メソッドを使用してフォーム コンテナーにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="cb87c-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb87c-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb87c-158">See also</span></span>



[<span data-ttu-id="cb87c-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="cb87c-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="cb87c-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb87c-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="cb87c-161">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cb87c-161">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

