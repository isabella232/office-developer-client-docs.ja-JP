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
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>管理容易性アプリケーションと Microsoft 365 アプリのクイック実行インストーラーの統合

Microsoft 365 アプリのクイック実行インストーラーをソフトウェア管理ソリューションと統合する方法について説明します。
  
Microsoft 365 Apps クイック実行インストーラーは、IT 担当者およびソフトウェア管理ソリューションが更新管理をプログラムで制御できるようにする COM インターフェイスを提供します。 このインターフェイスは、Office 展開ツールよりも高度な追加の管理機能を提供します。
  
> [!NOTE]
> この記事は、クイック実行インストーラーを使用している Office アプリに適用されます。 
  
## <a name="integrating-with-the-click-to-run"></a>クイック実行との統合

このインターフェイスを使用するには、管理アプリケーションで COM インターフェイスを起動して、クイック実行インストール サービスと直接通信する公開 API を呼び出します。 
  
> [!NOTE]
> [!メモ] Office クイック実行インストーラーは、インストーラーの動作を制御できるパラメーターを指定して、コマンド ラインから実行できます。詳細は、「[クイック実行用 Office 展開ツール](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)」を参照してください。 
  
**次に、COM インターフェイスの概念図を示します**

![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Office クイック実行インストーラーで COM インターフェイスを使用する図")
  
Microsoft 365 Apps クイック実行インストーラーは、 **IUpdateNotify** **CLSID_UpdateNotifyObject**に登録された COM ベースのインターフェイスを実装します。
  
このインターフェイスは、次のように呼び出すことができます。
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

クイック実行インストール プログラムは昇格された特権で実行する必要があるので、この呼び出しは、呼び出し元が昇格された特権で実行している場合のみ正常に実行されます。
  
**IUpdateNotify** COM インターフェイスは、コマンドおよびパラメーターの検証と、クイック実行インストール サービスによる実行のスケジュール設定に利用できる 3 つの非同期関数を公開しています。 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

4 つ目のメソッド **Status** は、最後に実行したコマンドの状態または現在実行中のコマンド状態に関する情報 (成功、失敗、詳細なエラー コードなど) を取得するために使用できます。
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

クイック実行インストール サービスには、そのライフサイクルの間に **IUpdateNotify** メソッドの呼び出しが可能になる 4 つの状態 (起動中、アイドル、ダウンロード中および適用中) が存在します。 
  
**次に、COM インターフェイスの状態マシンの図を示します**

![COM インターフェイスの状態ダイアグラムです。](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "COM インターフェイスの状態図")
  
> [!NOTE]
> **再起動**: コンピューターの起動時に、クイック実行インストーラーサービスが使用できない状態になります。 再起動後に Status メソッドの呼び出しが成功すると、eUPDATE_UNKNOWN が返されます。 
  
**Idle:** クイック実行インストーラーがアイドル状態のときは、以下を呼び出すことができます。 
  
- **Apply**: 以前にダウンロードしたコンテンツをインストールします。
    
- **Cancel**:  `0x800000e`「予期しないときにメソッドが呼び出されました。」を返します。
    
- **Download**: 後でインストールするために、新しいコンテンツをクライアントにダウンロードします。
    
- **Status**: 最後に完了したアクションの結果を返すか、アクションがエラーで終了した場合はエラー メッセージを返します。前のアクションがない場合は、 **Status** は  `eUPDATE_UNKNOWN` を返します。
    
**Downloading:** クイック実行インストーラーがダウンロード状態のときは、以下のものを呼び出すことができます。 
  
- **Apply**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。
    
- **Cancel**: ダウンロードを停止し、一部ダウンロードされたコンテンツを削除します。
    
- **Download**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。 
    
- **Status**: **DOWNLOAD_WIP** を返して、ダウンロード作業が進行中であることを示します。 
    
**適用中:** クイック実行インストーラーが、以前にダウンロードしたコンテンツのインストール処理中の場合。 
  
- **Apply**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。
    
- **Cancel**:  `0x800000e` を返します。Apply アクションを取り消すことはできません。
    
- **Download**: **HRESULT** `0x800000e` "予期しないときにメソッドが呼び出されました" という値を持つ HRESULT を返します。 
    
- **Status**: **APPLY_WIP** を返して、適用作業が進行中であることを示します。 
    
> [!NOTE]
> OfficeC2RCOM は COM+ サービスであり動的に読み込まれるコンポーネントであるため、期待どおりの結果が得られるようにするには、このクラスのメソッドを呼び出すたびに **CoCreateInstance** を呼び出す必要があります。 この COM+ サービスは必要に応じて新しいインスタンスの作成を処理します。 いずれかのメソッドが初めて呼び出されるときに、COM+ は **IUpdateNotify** オブジェクトを読み込んで、そのオブジェクトを dllhost.exe インスタンスの 1 つで実行します。 新しいオブジェクトは約 3 分間アイドル状態でアクティブになります。 前回の呼び出しから 3 分以内に後続の呼び出しが行われると、 **IUpdateNotify** オブジェクトは読み込まれたままで、新しいインスタンスは作成されません。 3 分以内に呼び出しが行われないと、IUpdateNotify オブジェクトはアンロードされ、その後の呼び出しでは新しい **IUpdateNotify** オブジェクトが作成されます。 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>クイック実行インストーラー COM API リファレンス ガイド

以下の API リファレンス ドキュメントでは、次のようになっています。
  
- パラメーターは、スペースで区切られたキー/値ペアの形式です。
    
- パラメーターでは大文字小文字は区別されません。
    
- [パラメーターのリスト](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/)と説明を利用できます。 
    
- IUpdateNotify2 インターフェイスの概要が含まれるようになりました。
    
### <a name="apply"></a>適用

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>パラメーター

-  _displaylevel_: 更新処理中のインストールの状態 (エラーを含む) を表示する場合は **true** に設定します。更新処理中のインストールの状態 (エラーを含む) を非表示にする場合は **false** に設定します。既定値は **false** です。
    
-  _forceappshutdown_: **Apply** アクションがトリガーされた直後に Office アプリケーションを強制的にシャット ダウンする場合は **true** に設定します。 **false** に設定した場合、実行中の Office アプリケーションがあると失敗します。既定値は **false** です。詳細は、「 [注釈](#bk_ApplyRemark)」を参照してください。 
    
  **Apply** アクションがトリガーされた時にいずれかの Office アプリケーションが実行中の場合、通常 **Apply** アクションは失敗します。  `forceappshutdown=true` が **Apply** メソッドに渡されると、 **OfficeClickToRun** サービスは即時にアプリケーションをシャットダウンし、更新プログラムを適用します。この場合、データの損失が発生する可能性があります。 
    
#### <a name="return-results"></a>返される結果

|||
|:-----|:-----|
|**S_OK** <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|**E_ACCESSDENIED** <br/> |呼び出し元が、昇格された特権で実行していません。  <br/> |
|**E_INVALIDARG** <br/> |無効なパラメーターが渡されました。  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_ApplyRemark)」を参照してください。  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>解説

- **Apply** アクションがトリガーされたときに実行中の Office アプリケーションがあると **Apply** アクションは失敗します。  `forceappshutdown=true` が **Apply** メソッドに渡されると、その直後に **OfficeClickToRun** サービスは実行中の Office アプリケーションをシャットダウンして更新プログラムを適用します。開いているドキュメントの変更内容を保存するように求めるダイアログが表示されないため、ユーザーはデータを損失する可能性があります。 
    
- このアクションは、COM の状態が次のいずれかのときにのみトリガーできます。 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- 以前にダウンロードしたコンテンツがない状態で **Apply** メソッドを呼び出すと、 **Apply** メソッドは **Succeeded** を報告します。これは、このメソッドが適用するものがないことを検出して、 **Apply** 処理を正常に完了したことを示します。 
    
### <a name="cancel"></a>キャンセル

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>返される結果

|||
|:-----|:-----|
|S_OK  <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_CancelRemarks)」セクションを参照してください。  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>解説

- このメソッドは、COM 状態 ID **eDOWNLOAD_WIP** の場合のみトリガーできます。このメソッドは現在のダウンロード アクションを取り消そうとします。COM 状態は **eDOWNLOAD_CANCELLING** に変わり、最終的に **eDOWNLOAD_CANCELED** に変わります。これ以外の場合にトリガーすると、COM 状態は **E_ILLEGAL_METHOD_CALL** を返します。 
    
### <a name="download"></a>ダウンロード

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>パラメーター

-  _displaylevel_: 更新処理中のインストールの状態 (エラーを含む) を表示する場合は **true** に設定します。更新処理中のインストールの状態 (エラーを含む) を非表示にする場合は **false** に設定します。既定値は **false** です。
    
-  _updatebaseurl_: 代替ダウンロード ソースへの URL です。
    
-  _updatetoversion_: このバージョンに Office を更新します。このパラメーターは、現在インストールされているバージョンよりも古いバージョンに更新する場合に定義します。
    
-  _downloadsource_: カスタマイズされた **IBackgroundCopyManager** の実装 (BITS マネージャー) の CLSID です。 
    
-  _contentid_: カスタマイズされた BITS マネージャーのコンテンツ サーバーからダウンロードするコンテンツを識別します。この値は、解釈のために BITS インターフェイスを介して渡されます。
    
#### <a name="return-results"></a>返される結果

|||
|:-----|:-----|
|**S_OK** <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|**E_ACCESSDENIED** <br/> |呼び出し元が、昇格された特権で実行していません。  <br/> |
|**E_INVALIDARG** <br/> |無効なパラメーターが渡されました。  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_DownloadRemark)」を参照してください。  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>解説

- _downloadsource_ と  _contentid_ をペアとして指定する必要があります。ペアで指定しないと、 **Download** メソッドは **E_INVALIDARG** エラーを返します。 
    
- _downloadsource_、 _contentid_、 _updatebaseurl_ を指定すると、  _updatebaseurl_ は無視されます。 
    
- このアクションは、COM の状態が次のいずれかのときにのみトリガーできます。 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- 以前にダウンロードしたコンテンツがない状態で **Apply** メソッドを呼び出すと、 **Apply** メソッドは **Succeeded** を報告します。それはこのメソッドが、適用されたものがないことを検出し、 **Apply** 処理を正常に完了したことを示します。 
    
#### <a name="examples"></a>例

- カスタマイズした BITS マネージャーからコンテンツをダウンロードするには、次のパラメーターを渡す **download()** 関数を呼び出します。 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Office コンテンツ配信ネットワーク (CDN) からコンテンツをダウンロードするには、 _downloadsource_、 _contentid_、または_updatebaseurl_パラメーターを指定せずに、 **download ()** 関数を呼び出します。 
    
- カスタマイズした場所からコンテンツをダウンロードするには、次のパラメーターを渡す **download()** 関数を呼び出します。 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>状態

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>パラメーター

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |UPDATE_STATUS_REPORT 構造体を指すポインターです。  <br/> |
   
#### <a name="return-results"></a>返される結果

|||
|:-----|:-----|
|**S_OK** <br/> |**Status** メソッドは、常にこの結果を返します。現在のアクションの状態については、  `UPDATE_STATUS_RESULT` 構造体を調べます。  <br/> |
   
#### <a name="remarks"></a>解説

- `UPDATE_STATUS_REPORT` の状態フィールドには、現在のアクションの状態が含まれています。次のいずれかの状態値が返されます。 
    
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

- 前回実行したコマンドがエラーになると、そのエラーに関する詳細が  `UPDATE_STATUS_REPORT` のエラー フィールドに入ります。2 種類のエラー コードが **Status** メソッドから返されます。 
    
- `UPDATE_ERROR_CODE::eUNKNOWN` より少ないエラーは、次の事前に定義されたエラー コードのいずれかになります。
    
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

  リターン エラー コードが  `UPDATE_ERROR_CODE::eUNKNOWN` より大きい場合、そのコードは失敗した関数呼び出しの **HRESULT** になります。HRESULT を抽出するには、  `UPDATE_ERROR_CODE::eUNKNOWN` のエラー フィールドで返された値から  `UPDATE_STATUS_REPORT` を減算します。
    
  状態とエラー値の完全なリストは、OfficeC2RCom.dll に埋め込まれている **IUpdateNotify** タイプ ライブラリを調べることで確認できます。 
    
- Contentid フィールドは、**ダウンロード**が開始された後の**状態**の呼び出しに使用され、**ダウンロード**呼び出しに渡された contentid を返します。 このフィールドは、 **Status** メソッドの呼び出し前に **null** に初期化し、 **Status** が返されてから値を確認するようにしてください。 この値が **null** のままの場合は、返す contentid がないことを意味します。 この値が **null** 以外の場合は、 **SysFreeString()** の呼び出しで解放する必要があります。 次のコード スニペットは、 **Download** の後で **Status** を呼び出す方法を示しています。
    
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

### <a name="summary-of-iupdatenotify2-interface"></a>IUpdateNotify2 インターフェイスの概要

バージョン [16.0.8208.6352] 新しい **IUpdateNotify2** インターフェイスが追加されました。 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- このインターフェイスは、下位互換性を実現するために元の IUpdateNotify インターフェイスもホストします。つまり、このインターフェイスを使用すると、 **UpdateNotifyObject** インターフェイスで提供されるすべてのメソッドにアクセスできるようになります。 
    
- IUpdateNotify2 には、次の新しいメソッドが追加されています。
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList)。更新をブロックしているアプリのリストを取得します。この呼び出しにより、更新処理の進行をブロックする実行中の Office アプリが返されます。 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData)。Office 展開データを取得します。 
    
- 新しいメソッドを使用する場合は、次のことを確認する必要があります。
    
  - Your C2R version is newer than the above build (\>= June fork build).
    
  - **CoCreateInstance** の呼び出しには、 **UpdateNotifyObject** ではなく UpdateNotifyObject2 を使用すること。
    
新しいメソッドを使用しない場合は、何も変更する必要はありません。すべての既存のメソッドは、以前とまったく同じ方法で動作します。
  
## <a name="implementing-the-bits-interface"></a>BITS インターフェイスの実装

[Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) は、クライアントとサーバーの間でファイルを転送するための Microsoft が提供するサービスです。 BITS は、Office クイック実行インストーラーがコンテンツのダウンロードに使用できるチャネルの 1 つです。 既定では、Microsoft 365 Apps クイック実行インストーラーは、Windows に組み込まれている BITS の実装を使用して、CDN からコンテンツをダウンロードします。 
  
カスタマイズされた BITS の実装を **IUpdateNotify** インターフェイスの **download()** メソッドに提供すると、管理ソフトウェアはクライアントがコンテンツをダウンロードする場所と方法を制御できます。 カスタマイズされた BITS インターフェイスは、CDN、IIS サーバー、ファイル共有など、クイック実行の組み込みチャネル以外のカスタムコンテンツ配布チャネルを提供する場合に便利です。 
  
カスタマイズした BITS インターフェイスが Office C2R サービスと連動するための最小要件は次のとおりです。
  
- **IBackgroundCopyManager** の場合:
    
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

- **IBackgroundCopyJob** の場合:
    
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

- **IBackgroundCopyJob3** の場合:
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- `Addfile` 関数と  `AddFileWithRanges` 関数の場合、リモート URL は次の形式です。 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits はハード コードされており、カスタマイズされた BITS を表します。
    
  -  _\<contentid\>_ は、 **Download ()** メソッドの_contentid_パラメーターです。 
    
  -  _\<relative path to target file\>_ ダウンロードするファイルの場所とファイル名を提供します。 
    
    たとえば、contentid () メソッドに対して_contentid_を提供していて、Office C2R がファイルなどのバージョン cab ファイルをダウンロードしようとしている場合は、 `f732af58-5d86-4299-abe9-7595c35136ef` **Download()** `v32.cab` **addfile ()** を次のように呼び出し `RemoteUrl` ます。
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- **IBackgroundCopyError** の場合:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- **IBackgroundCopyFile** の場合:
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a>コンテンツのステージングの自動化

IT 管理者は、Office 展開ツールまたは Microsoft エンドポイント構成マネージャーを使用して、更新プログラムチャネルから入手可能な更新プログラムの展開を制御することを選択することができます。
  
このサービスは、更新プログラムが利用可能になったときに、コンテンツのダウンロードを認識して自動化するための管理ツールの機能をサポートしています。
  
**次の画像は、カスタム イメージのダウンロードの概要です**

![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Office クイック実行インストーラーで COM インターフェイスを使用する図")
  
### <a name="overview-of-downloading-a-custom-image"></a>カスタム イメージのダウンロードの概要
  
前の図では、新しい Microsoft 365 アプリイメージが CDN で利用できることがわかります。 Microsoft 365 アプリの画像と共に、管理ソフトウェアが Office 展開ツールを使用する必要がある場合に、カスタマイズされた画像を直接作成できるようにするために必要な情報を持つ API が提供されています。

エンタープライズは、Microsoft 365 アプリの更新プログラムを同期するように WSUS を構成します。 こうした更新プログラムには実際のイメージ ペイロードは含まれていませんが、管理ソフトウェアは新しいコンテンツが利用可能になったことを認識できます。 管理性ソフトウェアは、Microsoft 365 アプリの更新プログラムメタデータを読み取って、更新プログラムが適用される Office のバージョンを理解できます。

更新プログラムの適用が可能な場合、管理ソフトウェアは CDN コンテンツとファイル リストを使用して、カスタム イメージを作成し、イメージの保存先として使用するように構成されたファイル共有の場所に保存できます。
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Microsoft 365 Apps ファイルリスト API の使用

Microsoft 365 Apps file list API は、Microsoft 365 アプリの特定の更新プログラムに必要なファイルの名前を取得するために使用されます。

HTTP 要求

GET https://config.office.com/api/filelist

このメソッドには、要求本文を指定しません。

この API を呼び出すために必要なアクセス許可はありません。

省略可能なクエリ パラメーター

|**名前**|**説明**|
|:-----|:-----|
| channel <br/>| チャネル名を指定します。  <br/> 省略可能。既定値は ' 半期 ' です。 <br/> サポートされる値 https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| バージョン <br/>| 更新プログラムのバージョンを指定します。 <br/> 省略可能。既定では、指定されたチャネルで利用可能な最新のバージョンを指定します。 |
| 建築 <br/>| クライアントアーキテクチャを指定します。 <br/> 省略可能。既定値は ' x64 ' です。 <br/> サポートされている値: x64、x86 |
| lid <br/>| 含める言語ファイルを指定します。 <br/> 省略可能。既定は [なし] <br/> 複数の言語を指定するには、言語ごとに lid のクエリパラメーターを含めます。 <br/> 言語識別子の形式 (例) を使用します。 ' en-us '、' fr-fr ' |
| alllanguages <br/>| すべての言語ファイルを含めるように指定します。 <br/> Optional –既定値は false です。 |

HTTP 応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。

イメージを作成するには、次の手順を実行します。
1.  API を呼び出して、目的の更新プログラムのチャネル、バージョン、およびアーキテクチャの適切なクエリパラメーターを提供します。
注: "lcid" という属性を持つファイルオブジェクトは、言語に依存しないファイルであり、イメージに含める必要があります。
2.  ファイルオブジェクトを反復処理し、CDN ファイルをコピーすることによって CDN のローカルイメージを構築し、各 file オブジェクトに定義された "relativePath" 属性で指定されているようにフォルダー構造を作成します。

次の例では、現在のチャネルのファイル一覧と64ビット版の16.0.4229.1004 を取得し、フランス語および英語の言語ファイルを含めます。

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>.Dat ファイルのハッシュ検証

イメージ作成ツールでは、計算されたハッシュ値と、各 .dat ファイルに関連付けられた指定のハッシュ値を比較することによって、ダウンロードした .dat ファイルの整合性を確認できます。 次に、hashLocation および hashAlgorithm の値を指定する file オブジェクトの例を示します。
  
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

- **Hashlocation**属性は、ハッシュ値を含む .cab ファイルの相対パスの場所を指定します。 URL + relativePath + hashLocation を連結して、ハッシュ ファイルの場所を構成します。 この例では、stream.x64.bg-bg.hash の場所は次のようになります。 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- **HashAlgorithm**属性は、使用されたハッシュアルゴリズムを指定します。 
    
  stream.x64.bg-bg.dat ファイルの整合性を検証するには、stream.x64.bg-bg.hash を開いて、ハッシュ ファイルの最初の行にあるハッシュ値を読み込みます。この値と処理済みのハッシュ値 (指定のハッシュ アルゴリズムを使用して計算された値) を比較して、ダウンロードした .dat ファイルの整合性を検証します。
    
  次の例は、ハッシュを読み取る C# コードを示しています。
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 アプリの更新プログラム

Microsoft のすべての365アプリの更新プログラムは、 [Microsoft Update カタログ](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)に公開されています。
  
Microsoft 365 アプリの更新により、管理ソフトウェアは、1つの例外を除き、他の WU 更新プログラムによく似た方法で Microsoft 365 アプリの更新を扱うことができます。クライアント更新プログラムには、実際のペイロードは含まれていません。 Microsoft 365 アプリの更新プログラムは、どのクライアントにもインストールしないでください。管理ソフトウェアを使用してワークフローを開始するには、上記のような COM ベースのインストールメカニズムを使用してインストールコマンドを置き換える必要があります。

**次の図は、Office 365 クライアント更新プログラムのワークフローを示しています。**

![O365PP クライアントの更新プログラムのワークフロー図です。](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "O365PP クライアント更新のワークフロー図")
  
公開されている Microsoft 365 アプリの更新プログラムには、更新プログラムに関するメタデータが含まれています。 このメタデータには、できる moreinfourl というパラメーターが含まれています。このパラメーターを使用すると、その特定の更新のためにファイルリスト API への API 呼び出しを派生させることができます。

次の例では、ファイルリスト API ができる moreinfourl に埋め込まれ、"ServicePath =" で始まります。

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>コンテンツステージングを自動化するための追加のメタデータ

**リリース履歴 API**
  
Microsoft 365 アプリのリリース履歴 API は、CDN に発行された各更新プログラムの詳細をチャネル名やその他のチャネル属性と共に取得するために使用されます。

HTTP 要求

```http
GET https://config.office.com/api/filelist/channels 
```

このメソッドには、要求本文を指定しません。

この API を呼び出すために必要なアクセス許可はありません。

HTTP 応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。

**Sku API**
  
Sku API は、さまざまなオプションとともに Office CDN からの展開とサービスの提供に使用できる製品を判断するのに役立つ情報を返します。

HTTP 要求

```http
GET https://config.office.com/api/filelist/skus 
```

このメソッドには、要求本文を指定しません。

この API を呼び出すために必要なアクセス許可はありません。

HTTP 応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文で file オブジェクトのコレクションを返します。
