---
title: 管理性アプリケーションとセキュリティ インストーラー Microsoft 365 Apps クイック実行統合
manager: lindalu
ms.date: 09/14/2021
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: ソフトウェア管理ソリューションとMicrosoft 365 Apps クイック実行インストーラーを統合する方法について説明します。
ms.openlocfilehash: 65f601dc81562a6aad8f19546f22f9948117d1af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554979"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>管理性アプリケーションとセキュリティ インストーラー Microsoft 365 Apps クイック実行統合

ソフトウェア管理ソリューションとMicrosoft 365 Apps クイック実行インストーラーを統合する方法について説明します。
  
このMicrosoft 365 Apps クイック実行は、IT プロフェッショナルとソフトウェア管理ソリューションが更新プログラムの管理をプログラムで制御できる COM インターフェイスを提供します。 このインターフェイスは、Office 展開ツールよりも高度な追加の管理機能を提供します。
  
> [!NOTE]
> この記事は、Officeインストーラーを使用するアプリクイック実行します。 
  
## <a name="integrating-with-the-click-to-run"></a>クイック実行との統合

このインターフェイスを使用するには、管理アプリケーションで COM インターフェイスを起動して、クイック実行インストール サービスと直接通信する公開 API を呼び出します。 
  
> [!NOTE]
> [!メモ] Office クイック実行インストーラーは、インストーラーの動作を制御できるパラメーターを指定して、コマンド ラインから実行できます。詳細は、「[クイック実行用 Office 展開ツール](/DeployOffice/overview-office-deployment-tool.md)」を参照してください。 
  
**次に、COM インターフェイスの概念図を示します**

![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Click-To-Run インストーラーで COM インターフェイスを使用Office図")
  
このMicrosoft 365 Apps クイック実行は COM ベースのインターフェイスを実装します **。IUpdateNotify** は **CLSID** に登録CLSID_UpdateNotifyObject。
  
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
> **再起動**: コンピューターが起動している場合、インストーラー サービスが使用できないクイック実行期間があります。 再起動後に Status メソッドの呼び出しが成功すると、eUPDATE_UNKNOWN が返されます。 
  
**Idle:** クイック実行インストーラーがアイドル状態のときは、以下を呼び出すことができます。 
  
- **Apply**: 以前にダウンロードしたコンテンツをインストールします。
    
- **Cancel**:  `0x800000e`「予期しないときにメソッドが呼び出されました。」を返します。
    
- **Download**: 後でインストールするために、新しいコンテンツをクライアントにダウンロードします。
    
- **Status**: 最後に完了したアクションの結果を返すか、アクションがエラーで終了した場合はエラー メッセージを返します。前のアクションがない場合は、 **Status** は  `eUPDATE_UNKNOWN` を返します。
    
**Downloading:** クイック実行インストーラーがダウンロード状態のときは、以下のものを呼び出すことができます。 
  
- **Apply**: "予期しない時刻にメソッドが呼び出された" という値の **HRESULT**  `0x800000e` を返します。
    
- **Cancel**: ダウンロードを停止し、一部ダウンロードされたコンテンツを削除します。
    
- **ダウンロード**: "予期しない時刻にメソッドが呼び出された" という値の **HRESULT**  `0x800000e` を返します。 
    
- **Status**: **DOWNLOAD_WIP** を返して、ダウンロード作業が進行中であることを示します。 
    
**適用中:** クイック実行インストーラーが、以前にダウンロードしたコンテンツのインストール処理中の場合。 
  
- **Apply**: "予期しない時刻にメソッドが呼び出された" という値の **HRESULT**  `0x800000e` を返します。
    
- **Cancel**:  `0x800000e` を返します。Apply アクションを取り消すことはできません。
    
- **ダウンロード**: "予期しない時刻にメソッドが呼び出された" という値の **HRESULT**  `0x800000e` を返します。 
    
- **Status**: **APPLY_WIP** を返して、適用作業が進行中であることを示します。 
    
> [!NOTE]
> OfficeC2RCOM は COM+ サービスであり動的に読み込まれるコンポーネントであるため、期待どおりの結果が得られるようにするには、このクラスのメソッドを呼び出すたびに **CoCreateInstance** を呼び出す必要があります。 この COM+ サービスは必要に応じて新しいインスタンスの作成を処理します。 いずれかのメソッドが初めて呼び出されるときに、COM+ は **IUpdateNotify** オブジェクトを読み込んで、そのオブジェクトを dllhost.exe インスタンスの 1 つで実行します。 新しいオブジェクトは約 3 分間アイドル状態でアクティブになります。 前回の呼び出しから 3 分以内に後続の呼び出しが行われると、 **IUpdateNotify** オブジェクトは読み込まれたままで、新しいインスタンスは作成されません。 3 分以内に呼び出しが行われないと、IUpdateNotify オブジェクトはアンロードされ、その後の呼び出しでは新しい **IUpdateNotify** オブジェクトが作成されます。 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>クイック実行インストーラー COM API リファレンス ガイド

以下の API リファレンス ドキュメントでは、次のようになっています。
  
- パラメーターは、スペースで区切られたキー/値ペアの形式です。
    
- パラメーターでは大文字小文字は区別されません。
    
- 詳細については、「インストールの[概要Office クイック実行関連するマルウェア対策アプリケーションについて」を参照してください](/office/troubleshoot/office-suite-issues/office-click-to-run-installation.md)。
    
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

|**結果**|**説明**|
|:-----|:-----|
|**S_OK** <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|**E_ACCESSDENIED** <br/> |呼び出し元が、昇格された特権で実行していません。  <br/> |
|**E_INVALIDARG** <br/> |無効なパラメーターが渡されました。  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_ApplyRemark)」を参照してください。  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>注釈

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

|**結果**|**Description**|
|:-----|:-----|
|S_OK  <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_CancelRemarks)」セクションを参照してください。  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>注釈

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

|**結果**|**説明**|
|:-----|:-----|
|**S_OK** <br/> |アクションが、実行のためにクイック実行サービスに正常に送られました。  <br/> |
|**E_ACCESSDENIED** <br/> |呼び出し元が、昇格された特権で実行していません。  <br/> |
|**E_INVALIDARG** <br/> |無効なパラメーターが渡されました。  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |この時点では、アクションは許可されていません。詳細については、「[注釈 ](#bk_DownloadRemark)」を参照してください。  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>注釈

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

- Office Content Delivery Network (CDN): **downloadsource、contentid、** または _updatebaseurl_ パラメーターを指定せずに _download()_ 関数を呼び出します。 
    
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

|**パラメーター**|**説明**|
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |UPDATE_STATUS_REPORT 構造体を指すポインターです。  <br/> |
   
#### <a name="return-results"></a>返される結果

|**結果**|**説明**|
|:-----|:-----|
|**S_OK** <br/> |**Status** メソッドは、常にこの結果を返します。現在のアクションの状態については、  `UPDATE_STATUS_RESULT` 構造体を調べます。  <br/> |
   
#### <a name="remarks"></a>注釈

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
    
- contentid フィールドは、ダウンロードが開始された後の **Status** の呼び出しに使用され、ダウンロード呼び出しに渡されたコンテンツ ID **を返** します。 このフィールドは、 **Status** メソッドの呼び出し前に **null** に初期化し、 **Status** が返されてから値を確認するようにしてください。 この値が **null** のままの場合は、返す contentid がないことを意味します。 この値が **null** 以外の場合は、 **SysFreeString()** の呼び出しで解放する必要があります。 次のコード スニペットは、 **Download** の後で **Status** を呼び出す方法を示しています。
    
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

バージョン [16.0.8208.6352] から、新しい **IUpdateNotify2** インターフェイスを追加しました。 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- このインターフェイスは、下位互換性を実現するために元の IUpdateNotify インターフェイスもホストします。つまり、このインターフェイスを使用すると、 **UpdateNotifyObject** インターフェイスで提供されるすべてのメソッドにアクセスできるようになります。 
    
- IUpdateNotify2 には、次の新しいメソッドが追加されています。
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList)。更新をブロックしているアプリのリストを取得します。この呼び出しにより、更新処理の進行をブロックする実行中の Office アプリが返されます。 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData)。Office 展開データを取得します。 
    
- 新しいメソッドを使用する場合は、以下を確認する必要があります。
    
  - Your C2R version is newer than the above build (\>= June fork build).
    
  - **CoCreateInstance** の呼び出しには、 **UpdateNotifyObject** ではなく UpdateNotifyObject2 を使用すること。
    
新しいメソッドを使用しない場合は、何も変更する必要はありません。すべての既存のメソッドは、以前とまったく同じ方法で動作します。
  
## <a name="implementing-the-bits-interface"></a>BITS インターフェイスの実装

[Background Intelligent Transfer Service](/windows/win32/bits/background-intelligent-transfer-service-portal.md) (BITS) は、クライアントとサーバーの間でファイルを転送するための Microsoft が提供するサービスです。 BITS は、Office クイック実行インストーラーがコンテンツのダウンロードに使用できるチャネルの 1 つです。 既定では、click-To-Run インストーラー Microsoft 365 Apps BITS の実装に組み込Windowsを使用して、コンテンツをダウンロードします。CDN。 
  
カスタマイズされた BITS の実装を **IUpdateNotify** インターフェイスの **download()** メソッドに提供すると、管理ソフトウェアはクライアントがコンテンツをダウンロードする場所と方法を制御できます。 カスタマイズされた BITS インターフェイスは、CDN、IIS サーバー、ファイル共有など、クイック実行 組み込みチャネル以外のカスタム コンテンツ配布チャネルを提供する場合に便利です。 
  
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
    
  -  _\<contentid\>_ は **Download()** メソッドの _contentid_ パラメーターです。 
    
  -  _\<relative path to target file\>_ ダウンロードするファイルの場所とファイル名を指定します。 
    
    たとえば、Download() メソッドに _contentid_ を指定し、Office C2R がファイルなどのバージョン cab ファイルをダウンロードする場合は `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **、AddFile()** を次のように呼び出します `RemoteUrl` 。
    
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

IT 管理者は、デスクトップ クライアントが CDN から直接利用可能な場合に更新プログラムを自動的に受信できるよう有効にするか、Office 展開ツールまたは Microsoft Endpoint Configuration Manager を使用して更新プログラム チャネルから利用可能な更新プログラムの展開を制御することもできます。
  
このサービスは、更新プログラムが利用可能になったときに、コンテンツのダウンロードを認識して自動化するための管理ツールの機能をサポートしています。
  
**次の画像は、カスタム イメージのダウンロードの概要です**

![Office クイック実行インストーラーで COM インターフェイスを使用する図です。](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Click-To-Run インストーラーで COM インターフェイスを使用Office図")
  
### <a name="overview-of-downloading-a-custom-image"></a>カスタム イメージのダウンロードの概要
  
前の図では、新しい画像がMicrosoft 365 Appsに表示CDN。 Microsoft 365 Apps イメージと共に、管理ソフトウェアがカスタマイズされたイメージを直接作成し、Office 展開ツールを使用する必要性を置き換える情報を含む API を使用できます。

企業は、更新プログラムを同期するために WSUS をMicrosoft 365 Appsします。 こうした更新プログラムには実際のイメージ ペイロードは含まれていませんが、管理ソフトウェアは新しいコンテンツが利用可能になったことを認識できます。 その後、管理ソフトウェアは更新プログラムMicrosoft 365 Appsメタデータを読み取り、更新プログラムが適用Officeバージョンを把握できます。

更新プログラムの適用が可能な場合、管理ソフトウェアは CDN コンテンツとファイル リストを使用して、カスタム イメージを作成し、イメージの保存先として使用するように構成されたファイル共有の場所に保存できます。
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>ファイルリスト API Microsoft 365 Apps使用する

ファイルMicrosoft 365 Apps API は、特定の更新プログラムに必要なファイルの名前を取得するためにMicrosoft 365 Appsされます。

HTTP 要求

GET https://config.office.com/api/filelist

このメソッドには、要求本文を指定しません。

この API を呼び出す権限は必要ありません。

省略可能なクエリ パラメーター

|**名前**|**説明**|
|:-----|:-----|
| チャネル <br/>| チャネル名を指定します。  <br/> 省略可能 – 既定値は 'SemiAnnual' <br/> サポートされている値 https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| 更新プログラムのバージョンを指定します。 <br/> 省略可能 – 指定したチャネルで使用できる最新バージョンの既定値 |
| arch <br/>| クライアント アーキテクチャを指定します。 <br/> 省略可能 – 既定値は 'x64' <br/> サポートされる値: x64、x86 |
| lid <br/>| 含める言語ファイルを指定します。 <br/> 省略可能 – 既定値はなし <br/> 複数の言語を指定するには、言語ごとに LID クエリ パラメーターを含めます。 <br/> 言語識別子の形式 (例) を使用します。 'ja-us', 'fr-fr' |
| alllanguages <br/>| すべての言語ファイルを含める場合に指定します。 <br/> 省略可能 – 既定値は false |

**HTTP 応答**

成功した場合、このメソッドは 200 OK 応答コードと、応答本文内のファイル オブジェクトのコレクションを返します。

イメージを作成するには、次の手順を実行します。
1.  API を呼び出し、関心のある更新プログラムのチャネル、バージョン、アーキテクチャに適切なクエリ パラメーターを提供します。
注: "lcid" という属性を持つファイル オブジェクト: "0" は言語に依存しないファイルであり、イメージに含める必要があります。
2.  各ファイル オブジェクトに対して定義されている "relativePath" 属性で指定されたフォルダー構造を作成しながら、ファイル オブジェクトを反復して CDN ファイルをコピーすることで、CDN のローカル イメージを作成します。

次の使用例は、現在のチャネルおよびバージョン 16.0.4229.1004 for 64bit のファイル 一覧を取得し、フランス語と英語の言語ファイルを含めます。

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>.dat ファイルのハッシュ検証

イメージ作成ツールは、計算されたハッシュ値と、各 .dat ファイルに関連付けられた指定されたハッシュ値を比較することで、ダウンロードした .dat ファイルの整合性を確認できます。 hashLocation 値と hashAlgorithm 値を指定するファイル オブジェクトの例を次に示します。
  
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

- **hashLocation 属性** は、ハッシュ値を含む.cabファイルの相対パスの場所を指定します。 URL + relativePath + hashLocation を連結して、ハッシュ ファイルの場所を構成します。 この例では、stream.x64.bg-bg.hash の場所は次のようになります。 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- **hashAlgorithm 属性は**、使用されたハッシュ アルゴリズムを指定します。 
    
  stream.x64.bg-bg.dat ファイルの整合性を検証するには、stream.x64.bg-bg.hash を開いて、ハッシュ ファイルの最初の行にあるハッシュ値を読み込みます。この値と処理済みのハッシュ値 (指定のハッシュ アルゴリズムを使用して計算された値) を比較して、ダウンロードした .dat ファイルの整合性を検証します。
    
  次の例は、ハッシュを読み取る C# コードを示しています。
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 Apps更新プログラム

すべての更新Microsoft 365 Apps Microsoft Update[カタログに発行されます](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)。
  
Microsoft 365 Apps更新プログラムを使用すると、管理ソフトウェアは、Microsoft 365 Apps更新プログラムを 1 つの例外を除き、他の WU 更新プログラムと非常に類似した方法で処理できます。クライアントの更新には、実際のペイロードは含めではありません。 Microsoft 365 Apps更新プログラムは、クライアントにインストールするのではなく、上記の COM ベースのインストール メカニズムでインストール コマンドを置き換える管理ソフトウェアを使用してワークフローをトリガーするために使用する必要があります。

**次の図は、Office 365 クライアント更新プログラムのワークフローを示しています。**

![O365PP クライアントの更新プログラムのワークフロー図です。](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "O365PP クライアント更新プログラムのワークフロー図")
  
発行Microsoft 365 Apps更新プログラムには、更新プログラムに関するメタデータが含まれます。 このメタデータには MoreInfoUrl というパラメーターが含まれています。このパラメーターを使用して、特定の更新プログラムのファイル リスト API への API 呼び出しを派生できます。

次の例では、ファイル リスト API は MoreInfoURL に埋め込まれているので、"ServicePath=" で始まります。

https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>コンテンツ ステージングを自動化する追加のメタデータ

**リリース履歴 API**
  
リリースMicrosoft 365 Apps API は、チャネル名や他のチャネル属性と共に、CDNに発行された各更新プログラムの詳細を取得するために使用されます。

HTTP 要求

```http
GET https://config.office.com/api/filelist/channels 
```

このメソッドには、要求本文を指定しません。

この API を呼び出す権限は必要ありません。

HTTP 応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文内のファイル オブジェクトのコレクションを返します。

**SKU API**
  
SKU API は、展開およびサービスに使用できる製品を特定する際に役立つ情報を、Office CDNオプションと共に返します。

HTTP 要求

```http
GET https://config.office.com/api/filelist/skus 
```

このメソッドには、要求本文を指定しません。

この API を呼び出す権限は必要ありません。

HTTP 応答

成功した場合、このメソッドは 200 OK 応答コードと、応答本文内のファイル オブジェクトのコレクションを返します。
