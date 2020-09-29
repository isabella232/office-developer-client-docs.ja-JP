---
title: 管理容易性アプリケーションと Microsoft 365 アプリのクイック実行インストーラーの統合
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Microsoft 365 アプリのクイック実行インストーラーをソフトウェア管理ソリューションと統合する方法について説明します。
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297315"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="19a68-103">管理容易性アプリケーションと Microsoft 365 アプリのクイック実行インストーラーの統合</span><span class="sxs-lookup"><span data-stu-id="19a68-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="19a68-104">Microsoft 365 アプリのクイック実行インストーラーをソフトウェア管理ソリューションと統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19a68-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="19a68-105">Microsoft 365 Apps クイック実行インストーラーは、IT 担当者およびソフトウェア管理ソリューションが更新管理をプログラムで制御できるようにする COM インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="19a68-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="19a68-106">このインターフェイスは、Office 展開ツールよりも高度な追加の管理機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="19a68-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="19a68-107">この記事は、クイック実行インストーラーを使用している Office アプリに適用されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="19a68-108">クイック実行との統合</span><span class="sxs-lookup"><span data-stu-id="19a68-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="19a68-109">このインターフェイスを使用するには、管理アプリケーションで COM インターフェイスを起動して、クイック実行インストール サービスと直接通信する公開 API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19a68-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="19a68-110">[!メモ] Office クイック実行インストーラーは、インストーラーの動作を制御できるパラメーターを指定して、コマンド ラインから実行できます。詳細は、「[クイック実行用 Office 展開ツール](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19a68-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="19a68-111">**次に、COM インターフェイスの概念図を示します**</span><span class="sxs-lookup"><span data-stu-id="19a68-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="19a68-112">![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Office クイック実行インストーラーで COM インターフェイスを使用する図")</span><span class="sxs-lookup"><span data-stu-id="19a68-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="19a68-113">Microsoft 365 Apps クイック実行インストーラーは、 **IUpdateNotify** **CLSID_UpdateNotifyObject**に登録された COM ベースのインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="19a68-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="19a68-114">このインターフェイスは、次のように呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="19a68-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="19a68-115">クイック実行インストール プログラムは昇格された特権で実行する必要があるので、この呼び出しは、呼び出し元が昇格された特権で実行している場合のみ正常に実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="19a68-116">**IUpdateNotify** COM インターフェイスは、コマンドおよびパラメーターの検証と、クイック実行インストール サービスによる実行のスケジュール設定に利用できる 3 つの非同期関数を公開しています。</span><span class="sxs-lookup"><span data-stu-id="19a68-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="19a68-117">4 つ目のメソッド **Status** は、最後に実行したコマンドの状態または現在実行中のコマンド状態に関する情報 (成功、失敗、詳細なエラー コードなど) を取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="19a68-118">クイック実行インストール サービスには、そのライフサイクルの間に **IUpdateNotify** メソッドの呼び出しが可能になる 4 つの状態 (起動中、アイドル、ダウンロード中および適用中) が存在します。</span><span class="sxs-lookup"><span data-stu-id="19a68-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="19a68-119">**次に、COM インターフェイスの状態マシンの図を示します**</span><span class="sxs-lookup"><span data-stu-id="19a68-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="19a68-120">![COM インターフェイスの状態ダイアグラムです。](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "COM インターフェイスの状態図")</span><span class="sxs-lookup"><span data-stu-id="19a68-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="19a68-121">**再起動**: コンピューターの起動時に、クイック実行インストーラーサービスが使用できない状態になります。</span><span class="sxs-lookup"><span data-stu-id="19a68-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="19a68-122">再起動後に Status メソッドの呼び出しが成功すると、eUPDATE_UNKNOWN が返されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="19a68-123">**Idle:** クイック実行インストーラーがアイドル状態のときは、以下を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="19a68-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="19a68-124">**Apply**: 以前にダウンロードしたコンテンツをインストールします。</span><span class="sxs-lookup"><span data-stu-id="19a68-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="19a68-125">**Cancel**:  `0x800000e`「予期しないときにメソッドが呼び出されました。」を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19a68-126">**Download**: 後でインストールするために、新しいコンテンツをクライアントにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="19a68-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="19a68-p103">**Status**: 最後に完了したアクションの結果を返すか、アクションがエラーで終了した場合はエラー メッセージを返します。前のアクションがない場合は、 **Status** は  `eUPDATE_UNKNOWN` を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p103">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure. If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="19a68-129">**Downloading:** クイック実行インストーラーがダウンロード状態のときは、以下のものを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="19a68-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="19a68-130">**Apply**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19a68-131">**Cancel**: ダウンロードを停止し、一部ダウンロードされたコンテンツを削除します。</span><span class="sxs-lookup"><span data-stu-id="19a68-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="19a68-132">**Download**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="19a68-133">**Status**: **DOWNLOAD_WIP** を返して、ダウンロード作業が進行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="19a68-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="19a68-134">**適用中:** クイック実行インストーラーが、以前にダウンロードしたコンテンツのインストール処理中の場合。</span><span class="sxs-lookup"><span data-stu-id="19a68-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="19a68-135">**Apply**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="19a68-136">**Cancel**:  `0x800000e` を返します。Apply アクションを取り消すことはできません。</span><span class="sxs-lookup"><span data-stu-id="19a68-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="19a68-137">**Download**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="19a68-138">**Status**: **APPLY_WIP** を返して、適用作業が進行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="19a68-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="19a68-139">OfficeC2RCOM は COM+ サービスであり動的に読み込まれるコンポーネントであるため、期待どおりの結果が得られるようにするには、このクラスのメソッドを呼び出すたびに **CoCreateInstance** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="19a68-140">この COM+ サービスは必要に応じて新しいインスタンスの作成を処理します。</span><span class="sxs-lookup"><span data-stu-id="19a68-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="19a68-141">いずれかのメソッドが初めて呼び出されるときに、COM+ は **IUpdateNotify** オブジェクトを読み込んで、そのオブジェクトを dllhost.exe インスタンスの 1 つで実行します。</span><span class="sxs-lookup"><span data-stu-id="19a68-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="19a68-142">新しいオブジェクトは約 3 分間アイドル状態でアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="19a68-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="19a68-143">前回の呼び出しから 3 分以内に後続の呼び出しが行われると、 **IUpdateNotify** オブジェクトは読み込まれたままで、新しいインスタンスは作成されません。</span><span class="sxs-lookup"><span data-stu-id="19a68-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="19a68-144">3 分以内に呼び出しが行われないと、IUpdateNotify オブジェクトはアンロードされ、その後の呼び出しでは新しい **IUpdateNotify** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="19a68-145">クイック実行インストーラー COM API リファレンス ガイド</span><span class="sxs-lookup"><span data-stu-id="19a68-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="19a68-146">以下の API リファレンス ドキュメントでは、次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="19a68-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="19a68-147">パラメーターは、スペースで区切られたキー/値ペアの形式です。</span><span class="sxs-lookup"><span data-stu-id="19a68-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="19a68-148">パラメーターでは大文字小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="19a68-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="19a68-149">[パラメーターのリスト](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/)と説明を利用できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="19a68-150">IUpdateNotify2 インターフェイスの概要が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="19a68-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="19a68-151">適用</span><span class="sxs-lookup"><span data-stu-id="19a68-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="19a68-152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19a68-152">Parameters</span></span>

-  <span data-ttu-id="19a68-p105">_displaylevel_: 更新処理中のインストールの状態 (エラーを含む) を表示する場合は **true** に設定します。更新処理中のインストールの状態 (エラーを含む) を非表示にする場合は **false** に設定します。既定値は **false** です。</span><span class="sxs-lookup"><span data-stu-id="19a68-p105">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process. The default is **false**.</span></span>
    
-  <span data-ttu-id="19a68-p106">_forceappshutdown_: **Apply** アクションがトリガーされた直後に Office アプリケーションを強制的にシャット ダウンする場合は **true** に設定します。 **false** に設定した場合、実行中の Office アプリケーションがあると失敗します。既定値は **false** です。詳細は、「 [注釈](#bk_ApplyRemark)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19a68-p106">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running. The default is **false**. See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="19a68-p107">**Apply** アクションがトリガーされた時にいずれかの Office アプリケーションが実行中の場合、通常 **Apply** アクションは失敗します。  `forceappshutdown=true` が **Apply** メソッドに渡されると、 **OfficeClickToRun** サービスは即時にアプリケーションをシャットダウンし、更新プログラムを適用します。この場合、データの損失が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-p107">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail. Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update. The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="19a68-161">返される結果</span><span class="sxs-lookup"><span data-stu-id="19a68-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a68-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19a68-162">**S_OK**</span></span> <br/> |<span data-ttu-id="19a68-163">アクションが、実行のためにクイック実行サービスに正常に送られました。</span><span class="sxs-lookup"><span data-stu-id="19a68-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19a68-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="19a68-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="19a68-165">呼び出し元が、昇格された特権で実行していません。</span><span class="sxs-lookup"><span data-stu-id="19a68-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="19a68-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="19a68-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="19a68-167">無効なパラメーターが渡されました。</span><span class="sxs-lookup"><span data-stu-id="19a68-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="19a68-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="19a68-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="19a68-p108">この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_ApplyRemark)」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="19a68-p108">Action is not allowed at this time. See [Remarks](#bk_ApplyRemark) for more information.  </span></span><br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="19a68-171">解説</span><span class="sxs-lookup"><span data-stu-id="19a68-171">Remarks</span></span>

- <span data-ttu-id="19a68-p109">**Apply** アクションがトリガーされたときに実行中の Office アプリケーションがあると **Apply** アクションは失敗します。  `forceappshutdown=true` が **Apply** メソッドに渡されると、その直後に **OfficeClickToRun** サービスは実行中の Office アプリケーションをシャットダウンして更新プログラムを適用します。開いているドキュメントの変更内容を保存するように求めるダイアログが表示されないため、ユーザーはデータを損失する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-p109">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail. Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update. The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="19a68-175">このアクションは、COM の状態が次のいずれかのときにのみトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="19a68-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="19a68-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="19a68-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="19a68-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="19a68-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="19a68-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19a68-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="19a68-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19a68-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19a68-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19a68-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19a68-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19a68-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="19a68-182">以前にダウンロードしたコンテンツがない状態で **Apply** メソッドを呼び出すと、 **Apply** メソッドは **Succeeded** を報告します。これは、このメソッドが適用するものがないことを検出して、 **Apply** 処理を正常に完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="19a68-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="19a68-183">キャンセル</span><span class="sxs-lookup"><span data-stu-id="19a68-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="19a68-184">返される結果</span><span class="sxs-lookup"><span data-stu-id="19a68-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a68-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="19a68-185">S_OK</span></span>  <br/> |<span data-ttu-id="19a68-186">アクションが、実行のためにクイック実行サービスに正常に送られました。</span><span class="sxs-lookup"><span data-stu-id="19a68-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19a68-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="19a68-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="19a68-p110">この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_CancelRemarks)」セクションを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="19a68-p110">Action is not allowed at this time. See the [Remarks](#bk_CancelRemarks) section for more information  </span></span><br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="19a68-190">解説</span><span class="sxs-lookup"><span data-stu-id="19a68-190">Remarks</span></span>

- <span data-ttu-id="19a68-p111">このメソッドは、COM 状態 ID **eDOWNLOAD_WIP** の場合のみトリガーできます。このメソッドは現在のダウンロード アクションを取り消そうとします。COM 状態は **eDOWNLOAD_CANCELLING** に変わり、最終的に **eDOWNLOAD_CANCELED** に変わります。これ以外の場合にトリガーすると、COM 状態は **E_ILLEGAL_METHOD_CALL** を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p111">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**. It will attempt to cancel the current download action. The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**. The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="19a68-195">ダウンロード</span><span class="sxs-lookup"><span data-stu-id="19a68-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="19a68-196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19a68-196">Parameters</span></span>

-  <span data-ttu-id="19a68-p112">_displaylevel_: 更新処理中のインストールの状態 (エラーを含む) を表示する場合は **true** に設定します。更新処理中のインストールの状態 (エラーを含む) を非表示にする場合は **false** に設定します。既定値は **false** です。</span><span class="sxs-lookup"><span data-stu-id="19a68-p112">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process. The default is **false**.</span></span>
    
-  <span data-ttu-id="19a68-199">_updatebaseurl_: 代替ダウンロード ソースへの URL です。</span><span class="sxs-lookup"><span data-stu-id="19a68-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="19a68-p113">_updatetoversion_: このバージョンに Office を更新します。このパラメーターは、現在インストールされているバージョンよりも古いバージョンに更新する場合に定義します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p113">_updatetoversion_: The version to update Office to. Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="19a68-202">_downloadsource_: カスタマイズされた **IBackgroundCopyManager** の実装 (BITS マネージャー) の CLSID です。</span><span class="sxs-lookup"><span data-stu-id="19a68-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="19a68-p114">_contentid_: カスタマイズされた BITS マネージャーのコンテンツ サーバーからダウンロードするコンテンツを識別します。この値は、解釈のために BITS インターフェイスを介して渡されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-p114">_contentid_: Identifies the content to download from the content server through the customized BITS manager. This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="19a68-205">返される結果</span><span class="sxs-lookup"><span data-stu-id="19a68-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a68-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19a68-206">**S_OK**</span></span> <br/> |<span data-ttu-id="19a68-207">アクションが、実行のためにクイック実行サービスに正常に送られました。</span><span class="sxs-lookup"><span data-stu-id="19a68-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="19a68-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="19a68-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="19a68-209">呼び出し元が、昇格された特権で実行していません。</span><span class="sxs-lookup"><span data-stu-id="19a68-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="19a68-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="19a68-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="19a68-211">無効なパラメーターが渡されました。</span><span class="sxs-lookup"><span data-stu-id="19a68-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="19a68-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="19a68-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="19a68-p115">この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_DownloadRemark)」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="19a68-p115">Action is not allowed at this time. See [Remarks](#bk_DownloadRemark) for more information.  </span></span><br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="19a68-215">解説</span><span class="sxs-lookup"><span data-stu-id="19a68-215">Remarks</span></span>

- <span data-ttu-id="19a68-p116">_downloadsource_ と  _contentid_ をペアとして指定する必要があります。ペアで指定しないと、 **Download** メソッドは **E_INVALIDARG** エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p116">You must specify  _downloadsource_ and  _contentid_ as a pair. If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="19a68-218">_downloadsource_、 _contentid_、 _updatebaseurl_ を指定すると、  _updatebaseurl_ は無視されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="19a68-219">このアクションは、COM の状態が次のいずれかのときにのみトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="19a68-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="19a68-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="19a68-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="19a68-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="19a68-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="19a68-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19a68-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="19a68-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19a68-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19a68-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="19a68-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="19a68-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="19a68-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="19a68-226">以前にダウンロードしたコンテンツがない状態で **Apply** メソッドを呼び出すと、 **Apply** メソッドは **Succeeded** を報告します。それはこのメソッドが、適用されたものがないことを検出し、 **Apply** 処理を正常に完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="19a68-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="19a68-227">例</span><span class="sxs-lookup"><span data-stu-id="19a68-227">Examples</span></span>

- <span data-ttu-id="19a68-228">カスタマイズした BITS マネージャーからコンテンツをダウンロードするには、次のパラメーターを渡す **download()** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19a68-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="19a68-229">Office コンテンツ配信ネットワーク (CDN) からコンテンツをダウンロードするには、 _downloadsource_、 _contentid_、または_updatebaseurl_パラメーターを指定せずに、 **download ()** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19a68-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="19a68-230">カスタマイズした場所からコンテンツをダウンロードするには、次のパラメーターを渡す **download()** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="19a68-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="19a68-231">状態</span><span class="sxs-lookup"><span data-stu-id="19a68-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="19a68-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19a68-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="19a68-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="19a68-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="19a68-234">UPDATE_STATUS_REPORT 構造体を指すポインターです。</span><span class="sxs-lookup"><span data-stu-id="19a68-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="19a68-235">返される結果</span><span class="sxs-lookup"><span data-stu-id="19a68-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a68-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="19a68-236">**S_OK**</span></span> <br/> |<span data-ttu-id="19a68-p117">**Status** メソッドは、常にこの結果を返します。現在のアクションの状態については、  `UPDATE_STATUS_RESULT` 構造体を調べます。  </span><span class="sxs-lookup"><span data-stu-id="19a68-p117">The **Status** method always returns this result. Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.  </span></span><br/> |
   
#### <a name="remarks"></a><span data-ttu-id="19a68-239">解説</span><span class="sxs-lookup"><span data-stu-id="19a68-239">Remarks</span></span>

- <span data-ttu-id="19a68-p118">`UPDATE_STATUS_REPORT` の状態フィールドには、現在のアクションの状態が含まれています。次のいずれかの状態値が返されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-p118">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action. One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="19a68-p119">前回実行したコマンドがエラーになると、そのエラーに関する詳細が  `UPDATE_STATUS_REPORT` のエラー フィールドに入ります。2 種類のエラー コードが **Status** メソッドから返されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-p119">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error. Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="19a68-244">`UPDATE_ERROR_CODE::eUNKNOWN` より少ないエラーは、次の事前に定義されたエラー コードのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="19a68-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="19a68-p120">リターン エラー コードが  `UPDATE_ERROR_CODE::eUNKNOWN` より大きい場合、そのコードは失敗した関数呼び出しの **HRESULT** になります。HRESULT を抽出するには、  `UPDATE_ERROR_CODE::eUNKNOWN` のエラー フィールドで返された値から  `UPDATE_STATUS_REPORT` を減算します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p120">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call. To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="19a68-247">状態とエラー値の完全なリストは、OfficeC2RCom.dll に埋め込まれている **IUpdateNotify** タイプ ライブラリを調べることで確認できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="19a68-248">Contentid フィールドは、**ダウンロード**が開始された後の**状態**の呼び出しに使用され、**ダウンロード**呼び出しに渡された contentid を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="19a68-249">このフィールドは、 **Status** メソッドの呼び出し前に **null** に初期化し、 **Status** が返されてから値を確認するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="19a68-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="19a68-250">この値が **null** のままの場合は、返す contentid がないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="19a68-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="19a68-251">この値が **null** 以外の場合は、 **SysFreeString()** の呼び出しで解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="19a68-252">次のコード スニペットは、 **Download** の後で **Status** を呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="19a68-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="19a68-253">IUpdateNotify2 インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="19a68-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="19a68-254">バージョン [16.0.8208.6352] 新しい **IUpdateNotify2** インターフェイスが追加されました。</span><span class="sxs-lookup"><span data-stu-id="19a68-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="19a68-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="19a68-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="19a68-p122">このインターフェイスは、下位互換性を実現するために元の IUpdateNotify インターフェイスもホストします。つまり、このインターフェイスを使用すると、 **UpdateNotifyObject** インターフェイスで提供されるすべてのメソッドにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="19a68-p122">This interface also hosted the original IUpdateNotify interface to provide backward compatibility. Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="19a68-258">IUpdateNotify2 には、次の新しいメソッドが追加されています。</span><span class="sxs-lookup"><span data-stu-id="19a68-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="19a68-p123">**HRESULT** GetBlockingApps([out] BSTR \* AppsList)。更新をブロックしているアプリのリストを取得します。この呼び出しにより、更新処理の進行をブロックする実行中の Office アプリが返されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-p123">**HRESULT** GetBlockingApps([out] BSTR \* AppsList). Get updates blocking apps list. This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="19a68-p124">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData)。Office 展開データを取得します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p124">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData). Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="19a68-264">新しいメソッドを使用する場合は、次のことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="19a68-265">Your C2R version is newer than the above build (\>= June fork build).</span><span class="sxs-lookup"><span data-stu-id="19a68-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="19a68-266">**CoCreateInstance** の呼び出しには、 **UpdateNotifyObject** ではなく UpdateNotifyObject2 を使用すること。</span><span class="sxs-lookup"><span data-stu-id="19a68-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="19a68-p125">新しいメソッドを使用しない場合は、何も変更する必要はありません。すべての既存のメソッドは、以前とまったく同じ方法で動作します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p125">If you don't use any of the new methods, you don't need to change anything. All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="19a68-269">BITS インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="19a68-269">Implementing the BITS interface</span></span>

<span data-ttu-id="19a68-270">[Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) は、クライアントとサーバーの間でファイルを転送するための Microsoft が提供するサービスです。</span><span class="sxs-lookup"><span data-stu-id="19a68-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="19a68-271">BITS は、Office クイック実行インストーラーがコンテンツのダウンロードに使用できるチャネルの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="19a68-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="19a68-272">既定では、Microsoft 365 Apps クイック実行インストーラーは、Windows に組み込まれている BITS の実装を使用して、CDN からコンテンツをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="19a68-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="19a68-273">カスタマイズされた BITS の実装を **IUpdateNotify** インターフェイスの **download()** メソッドに提供すると、管理ソフトウェアはクライアントがコンテンツをダウンロードする場所と方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="19a68-274">カスタマイズされた BITS インターフェイスは、CDN、IIS サーバー、ファイル共有など、クイック実行の組み込みチャネル以外のカスタムコンテンツ配布チャネルを提供する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="19a68-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="19a68-275">カスタマイズした BITS インターフェイスが Office C2R サービスと連動するための最小要件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="19a68-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="19a68-276">**IBackgroundCopyManager** の場合:</span><span class="sxs-lookup"><span data-stu-id="19a68-276">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="19a68-277">**IBackgroundCopyJob** の場合:</span><span class="sxs-lookup"><span data-stu-id="19a68-277">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="19a68-278">**IBackgroundCopyJob3** の場合:</span><span class="sxs-lookup"><span data-stu-id="19a68-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="19a68-279">`Addfile` 関数と  `AddFileWithRanges` 関数の場合、リモート URL は次の形式です。</span><span class="sxs-lookup"><span data-stu-id="19a68-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="19a68-280">cmbits はハード コードされており、カスタマイズされた BITS を表します。</span><span class="sxs-lookup"><span data-stu-id="19a68-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="19a68-281">_\<contentid\>_ は、 **Download ()** メソッドの_contentid_パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="19a68-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="19a68-282">_\<relative path to target file\>_ ダウンロードするファイルの場所とファイル名を提供します。</span><span class="sxs-lookup"><span data-stu-id="19a68-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="19a68-283">たとえば、contentid () メソッドに対して_contentid_を提供していて、Office C2R がファイルなどのバージョン cab ファイルをダウンロードしようとしている場合は、 `f732af58-5d86-4299-abe9-7595c35136ef` **Download()** `v32.cab` **addfile ()** を次のように呼び出し `RemoteUrl` ます。</span><span class="sxs-lookup"><span data-stu-id="19a68-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="19a68-284">**IBackgroundCopyError** の場合:</span><span class="sxs-lookup"><span data-stu-id="19a68-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="19a68-285">**IBackgroundCopyFile** の場合:</span><span class="sxs-lookup"><span data-stu-id="19a68-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="19a68-286">コンテンツのステージングの自動化</span><span class="sxs-lookup"><span data-stu-id="19a68-286">Automating content staging</span></span>

<span data-ttu-id="19a68-287">IT 管理者は、Office 展開ツールまたは Microsoft エンドポイント構成マネージャーを使用して、更新プログラムチャネルから入手可能な更新プログラムの展開を制御することを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="19a68-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="19a68-288">このサービスは、更新プログラムが利用可能になったときに、コンテンツのダウンロードを認識して自動化するための管理ツールの機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="19a68-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="19a68-289">**次の画像は、カスタム イメージのダウンロードの概要です**</span><span class="sxs-lookup"><span data-stu-id="19a68-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="19a68-290">![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Office クイック実行インストーラーで COM インターフェイスを使用する図")</span><span class="sxs-lookup"><span data-stu-id="19a68-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="19a68-291">カスタム イメージのダウンロードの概要</span><span class="sxs-lookup"><span data-stu-id="19a68-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="19a68-292">前の図では、新しい Microsoft 365 アプリイメージが CDN で利用できることがわかります。</span><span class="sxs-lookup"><span data-stu-id="19a68-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="19a68-293">Microsoft 365 アプリの画像と共に、管理ソフトウェアが Office 展開ツールを使用する必要がある場合に、カスタマイズされた画像を直接作成できるようにするために必要な情報を持つ API が提供されています。</span><span class="sxs-lookup"><span data-stu-id="19a68-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="19a68-294">エンタープライズは、Microsoft 365 アプリの更新プログラムを同期するように WSUS を構成します。</span><span class="sxs-lookup"><span data-stu-id="19a68-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="19a68-295">こうした更新プログラムには実際のイメージ ペイロードは含まれていませんが、管理ソフトウェアは新しいコンテンツが利用可能になったことを認識できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="19a68-296">管理性ソフトウェアは、Microsoft 365 アプリの更新プログラムメタデータを読み取って、更新プログラムが適用される Office のバージョンを理解できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="19a68-297">更新プログラムの適用が可能な場合、管理ソフトウェアは CDN コンテンツとファイル リストを使用して、カスタム イメージを作成し、イメージの保存先として使用するように構成されたファイル共有の場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="19a68-298">Microsoft 365 Apps ファイルリスト API の使用</span><span class="sxs-lookup"><span data-stu-id="19a68-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="19a68-299">Microsoft 365 Apps file list API は、Microsoft 365 アプリの特定の更新プログラムに必要なファイルの名前を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="19a68-300">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="19a68-300">HTTP Request</span></span>

<span data-ttu-id="19a68-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="19a68-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="19a68-302">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="19a68-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="19a68-303">この API を呼び出すために必要なアクセス許可はありません。</span><span class="sxs-lookup"><span data-stu-id="19a68-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="19a68-304">省略可能なクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="19a68-304">Optional query parameters</span></span>

|<span data-ttu-id="19a68-305">**名前**</span><span class="sxs-lookup"><span data-stu-id="19a68-305">**Name**</span></span>|<span data-ttu-id="19a68-306">**説明**</span><span class="sxs-lookup"><span data-stu-id="19a68-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="19a68-307">channel</span><span class="sxs-lookup"><span data-stu-id="19a68-307">channel</span></span> <br/>| <span data-ttu-id="19a68-308">チャネル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="19a68-309">省略可能。既定値は ' 半期 ' です。</span><span class="sxs-lookup"><span data-stu-id="19a68-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="19a68-310">サポートされる値 https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="19a68-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="19a68-311">バージョン</span><span class="sxs-lookup"><span data-stu-id="19a68-311">version</span></span> <br/>| <span data-ttu-id="19a68-312">更新プログラムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-312">Specifies the update version</span></span> <br/> <span data-ttu-id="19a68-313">省略可能。既定では、指定されたチャネルで利用可能な最新のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="19a68-314">建築</span><span class="sxs-lookup"><span data-stu-id="19a68-314">arch</span></span> <br/>| <span data-ttu-id="19a68-315">クライアントアーキテクチャを指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="19a68-316">省略可能。既定値は ' x64 ' です。</span><span class="sxs-lookup"><span data-stu-id="19a68-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="19a68-317">サポートされている値: x64、x86</span><span class="sxs-lookup"><span data-stu-id="19a68-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="19a68-318">lid</span><span class="sxs-lookup"><span data-stu-id="19a68-318">lid</span></span> <br/>| <span data-ttu-id="19a68-319">含める言語ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="19a68-320">省略可能。既定は [なし]</span><span class="sxs-lookup"><span data-stu-id="19a68-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="19a68-321">複数の言語を指定するには、言語ごとに lid のクエリパラメーターを含めます。</span><span class="sxs-lookup"><span data-stu-id="19a68-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="19a68-322">言語識別子の形式 (例) を使用します。</span><span class="sxs-lookup"><span data-stu-id="19a68-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="19a68-323">' en-us '、' fr-fr '</span><span class="sxs-lookup"><span data-stu-id="19a68-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="19a68-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="19a68-324">alllanguages</span></span> <br/>| <span data-ttu-id="19a68-325">すべての言語ファイルを含めるように指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="19a68-326">Optional –既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="19a68-326">Optional – defaults to false</span></span> |

<span data-ttu-id="19a68-327">HTTP 応答</span><span class="sxs-lookup"><span data-stu-id="19a68-327">HTTP Response</span></span>

<span data-ttu-id="19a68-328">成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="19a68-329">イメージを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="19a68-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="19a68-330">API を呼び出して、目的の更新プログラムのチャネル、バージョン、およびアーキテクチャの適切なクエリパラメーターを提供します。</span><span class="sxs-lookup"><span data-stu-id="19a68-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="19a68-331">注: "lcid" という属性を持つファイルオブジェクトは、言語に依存しないファイルであり、イメージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="19a68-332">ファイルオブジェクトを反復処理し、CDN ファイルをコピーすることによって CDN のローカルイメージを構築し、各 file オブジェクトに定義された "relativePath" 属性で指定されているようにフォルダー構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="19a68-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="19a68-333">次の例では、現在のチャネルのファイル一覧と64ビット版の16.0.4229.1004 を取得し、フランス語および英語の言語ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="19a68-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="19a68-334">.Dat ファイルのハッシュ検証</span><span class="sxs-lookup"><span data-stu-id="19a68-334">Hash verification of .dat files</span></span>

<span data-ttu-id="19a68-335">イメージ作成ツールでは、計算されたハッシュ値と、各 .dat ファイルに関連付けられた指定のハッシュ値を比較することによって、ダウンロードした .dat ファイルの整合性を確認できます。</span><span class="sxs-lookup"><span data-stu-id="19a68-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="19a68-336">次に、hashLocation および hashAlgorithm の値を指定する file オブジェクトの例を示します。</span><span class="sxs-lookup"><span data-stu-id="19a68-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="19a68-337">**Hashlocation**属性は、ハッシュ値を含む .cab ファイルの相対パスの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="19a68-338">URL + relativePath + hashLocation を連結して、ハッシュ ファイルの場所を構成します。</span><span class="sxs-lookup"><span data-stu-id="19a68-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="19a68-339">この例では、stream.x64.bg-bg.hash の場所は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="19a68-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="19a68-340">**HashAlgorithm**属性は、使用されたハッシュアルゴリズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="19a68-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="19a68-p134">stream.x64.bg-bg.dat ファイルの整合性を検証するには、stream.x64.bg-bg.hash を開いて、ハッシュ ファイルの最初の行にあるハッシュ値を読み込みます。この値と処理済みのハッシュ値 (指定のハッシュ アルゴリズムを使用して計算された値) を比較して、ダウンロードした .dat ファイルの整合性を検証します。</span><span class="sxs-lookup"><span data-stu-id="19a68-p134">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file. Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="19a68-343">次の例は、ハッシュを読み取る C# コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="19a68-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="19a68-344">Microsoft 365 アプリの更新プログラム</span><span class="sxs-lookup"><span data-stu-id="19a68-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="19a68-345">Microsoft のすべての365アプリの更新プログラムは、 [Microsoft Update カタログ](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)に公開されています。</span><span class="sxs-lookup"><span data-stu-id="19a68-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="19a68-346">Microsoft 365 アプリの更新により、管理ソフトウェアは、1つの例外を除き、他の WU 更新プログラムによく似た方法で Microsoft 365 アプリの更新を扱うことができます。クライアント更新プログラムには、実際のペイロードは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="19a68-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="19a68-347">Microsoft 365 アプリの更新プログラムは、どのクライアントにもインストールしないでください。管理ソフトウェアを使用してワークフローを開始するには、上記のような COM ベースのインストールメカニズムを使用してインストールコマンドを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a68-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="19a68-348">**次の図は、Office 365 クライアント更新プログラムのワークフローを示しています。**</span><span class="sxs-lookup"><span data-stu-id="19a68-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="19a68-349">![O365PP クライアントの更新プログラムのワークフロー図です。](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "O365PP クライアント更新のワークフロー図")</span><span class="sxs-lookup"><span data-stu-id="19a68-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="19a68-350">公開されている Microsoft 365 アプリの更新プログラムには、更新プログラムに関するメタデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="19a68-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="19a68-351">このメタデータには、できる moreinfourl というパラメーターが含まれています。このパラメーターを使用すると、その特定の更新のためにファイルリスト API への API 呼び出しを派生させることができます。</span><span class="sxs-lookup"><span data-stu-id="19a68-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="19a68-352">次の例では、ファイルリスト API ができる moreinfourl に埋め込まれ、"ServicePath =" で始まります。</span><span class="sxs-lookup"><span data-stu-id="19a68-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="19a68-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="19a68-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="19a68-354">コンテンツステージングを自動化するための追加のメタデータ</span><span class="sxs-lookup"><span data-stu-id="19a68-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="19a68-355">**リリース履歴 API**</span><span class="sxs-lookup"><span data-stu-id="19a68-355">**Release History API**</span></span>
  
<span data-ttu-id="19a68-356">Microsoft 365 アプリのリリース履歴 API は、CDN に発行された各更新プログラムの詳細をチャネル名やその他のチャネル属性と共に取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="19a68-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="19a68-357">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="19a68-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="19a68-358">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="19a68-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="19a68-359">この API を呼び出すために必要なアクセス許可はありません。</span><span class="sxs-lookup"><span data-stu-id="19a68-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="19a68-360">HTTP 応答</span><span class="sxs-lookup"><span data-stu-id="19a68-360">HTTP Response</span></span>

<span data-ttu-id="19a68-361">成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="19a68-362">**Sku API**</span><span class="sxs-lookup"><span data-stu-id="19a68-362">**SKUs API**</span></span>
  
<span data-ttu-id="19a68-363">Sku API は、さまざまなオプションとともに Office CDN からの展開とサービスの提供に使用できる製品を判断するのに役立つ情報を返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="19a68-364">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="19a68-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="19a68-365">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="19a68-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="19a68-366">この API を呼び出すために必要なアクセス許可はありません。</span><span class="sxs-lookup"><span data-stu-id="19a68-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="19a68-367">HTTP 応答</span><span class="sxs-lookup"><span data-stu-id="19a68-367">HTTP Response</span></span>

<span data-ttu-id="19a68-368">成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="19a68-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
