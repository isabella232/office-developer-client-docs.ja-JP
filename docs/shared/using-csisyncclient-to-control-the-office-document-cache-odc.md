---
title: Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用法について取り上げます。
ms.openlocfilehash: adaa56bf040889bd8220506bcfab8fdb0b7ab6c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804732"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用

Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用法について取り上げます。
  
CSISyncClient はアウトプロセス COM サーバー (CsiSyncClient.exe) で、Microsoft OneDrive はこれを使用して Office ドキュメント キャッシュ (ODC) の動作を制御できます。たとえば、OneDrive は CSISyncClient を介して ODC を呼び出し、MS-FSSHTTP 対応エンドポイントとの間でファイルのアップロードおよびダウンロードを実行することができます。このようにすると、共同編集や、オフラインからオンラインへのシームレスな移行など Office における下位サービス機能を活用できます。
  
CsiSyncClient は Office デスクトップ (x86 と x64) で利用できます。注: 新しいバージョンの Office には CsiSyncClient が同梱されていますが、このプロセスを使用できるのは下位互換性のために限定されます。ODC を制御するための CsiSyncClient インターフェイスとメソドロジは今後のバージョンの Office で変更される予定です。
  
現在、クラス ID は OneDrive にのみ応答するように設定されています。
  
COM オブジェクトはアウトプロセス COM サーバーとして使用でき、CsiSyncClient.exe で実行されます。(ODC が使用する) Access の制約のため、Office のビット種類と同じものが、つまり x64 Office では x64 COM オブジェクト、x86 Office では x86 COM オブジェクトがそれぞれ同梱されています。この制約を回避するため、CLSCTX_LOCAL_SERVER を CoCreateInstance の一部として指定すると、アウトプロセス COM サーバーとして COM オブジェクトがホストされ、ビット互換性が確保されます。
  
## <a name="interfaces"></a>インターフェイス

CSISyncClient は以下のインターフェイスを使用します。
  
### <a name="interface-ilsclocalsyncclient"></a>インターフェイス ILSCLocalSyncClient

これは、Office でファイルを同期するために使用するプライマリ インターフェイスです。
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
公開されているこの COM オブジェクトはアウトプロセス サーバーとして使用されます。CLSCTX_LOCAL_SERVER を CoCreateInstance の一部として指定すると、64 ビットと 32 ビットのプロセス間で互換性が得られます。
  
COM オブジェクトを共同作成した後、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)を最初に呼び出す必要があります。[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)が正常に完了した後には、任意の API を何度でも希望する順序で呼び出すことができます。また、既に初期化されたオブジェクトで [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)を呼び出すことができますが、呼び出しても何も実行されません。 
  
前述の段落の例外は、[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache)と [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)です。[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)を COM オブジェクトで呼び出した後、このオブジェクトを破棄し、新しいオブジェクトを作成する必要があります。[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache)はサブキャッシュを削除し、そのキャッシュ内のすべての関連ファイル情報を削除しますが、ディスク上のドキュメントはそのままにします。また、キャッシュとの通信のための状態もそのままになります。それにより、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) を再び呼び出して、COM オブジェクトを破棄してから再作成することなく、新しいキャッシュを作成できます。 
  
**パブリック メンバー関数**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile は、キャッシュからファイル情報を削除する場合に使用します。ただし、このメソッドはディスクとサーバー上の関連ファイルはそのままにします。
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>パラメーター

 _bstrResourceID_
  
ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_LSC_FILENOTFOUND  <br/> |指定された ResourceID がキャッシュにありません。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |これまでに、Initialize が正常に呼び出されなかったことがあります。  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |現在、ファイルが同期中または開かれた状態であるため、削除できません。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges は ILSCEvent オブジェクトの列挙子を返します。また、GetChanges の次の呼び出しに提供されたトークンも返します。その場合、それまでのイベント セットの処理をコンシューマーが完了したと想定されます。指定された  _nPreviousChangesToken_ より前のイベントは、削除され、使用できません。処理するイベントがない場合、  _pnCurrentChangesToken_ の値は  _nPreviousChangesToken_ と同じになりますが、  _ppiEvents_ は引き続き設定されます。 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>パラメーター

 _nPreviousChangesToken_
  
コンシューマーによって最後に処理されたイベントを示します。 
  
 _pnCurrentChangesToken_
  
コンシューマーに渡された最新のイベントを示します。Null にはできません。
  
 _ppiEvents_
  
コンシューマーに渡されたイベントの列挙子。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission は、ネットワーク コストと消費電力に関する Office の同期ヒューリスティックを上書きするかどうかを照会するときに使用します。3G やその他の高コストのネットワークの場合、または電源に接続されているのではなくバッテリーで稼働している場合には、適切なときまでネットワーク トラフィックをブロックするように Office で選択することができます。
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>パラメーター

 _nspType_
  
照会対象のコスト ヒューリスティックを定義するフラグ。「[列挙 LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)」をご覧ください。 
  
 _pfSyncEnabled_
  
要求されたコスト ヒューリスティックを現在上書きするかどうかを指定します。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus は、特定のファイルに関する情報、つまり、キャッシュ内に存在するかどうか、サーバー コピーとの通信が保留されているかどうか、Office 2013 に含まれているデータがローカル コピーからの最新データかどうかなどの情報を収集するために使用されます。CsiSyncClient COM オブジェクトが照会する情報を判別するには、[列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 値のビット単位のフラグが必要です。 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>パラメーター

 _bstrResourceID_
  
クライアント上のファイルを示す文字列。この値を空にすることはできません。最大長は 128 文字です。 
  
 _sfRequestedStatus_
  
返す情報を定義するフラグ。「[列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)」をご覧ください。 
  
 _pbstrFileSystemPath_
  
クライアント上の  _bstrResourceID_ によって識別されるファイルの場所を示す文字列。Null にはできません。 
  
 _pbstrETag_
  
_bstrResourceID_ によって識別されるファイルの eTag が入る文字列。Null にはできません。 
  
 _psfFileStatus_
  
_bstrResourceID_ によって識別されるファイルに関して、  _sfRequestedStatus_ を介して要求されるステータスが含まれるフラグ。Null にはできません。「 [列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)」をご覧くださいい。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_FILENOTFOUND  <br/> |_bstrResourceID_ によって指定されたファイル情報がキャッシュ内にありません。  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged が要求されたか、 _bstrResourceID_ によって指定されたファイルがロックされているか、または存在しません。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions は、現在 CsiSyncClient COM オブジェクトによってサポートされているパイプ区切りファイル拡張子の一覧を返します。この一覧は変更される可能性があります。コンシューマーは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)で提供される IPartnerActivityCallback オブジェクトを介して変更を通知されます (EventOccured をご覧ください)。 
  
戻される文字列の例: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>パラメーター

 _pbstrSupportedFileExtensions_
  
CsiSyncClient COM オブジェクトによってサポートされているファイル拡張子のパイプ区切りセットで設定する文字列。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

呼び出される最初のメソッドは、Initialize でなければなりません。そうでない場合には、他のすべての API は E_LSC_NOTINITIALIZED を返します。既に初期化されたオブジェクトで Initialize を呼び出すと、S_OK が戻り、何も実行されません。E_LSC_CACHEMISMATCH が戻る場合には、呼び出し側は [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) を呼び出して、指定の SuppliedID と関連付けられているキャッシュを削除できます。ただし、その場合には他の API では E_LSC_NOTINITIALIZED がやはり戻ります。 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>パラメーター

 _bstrSuppliedID_
  
コンシューマー、および使用するキャッシュを示します。空にすることはできず、最大長は 32 文字です。 
  
 _bstrProgID_
  
双方向通信のためのコンシューマーの COM オブジェクトを示します。空にすることはできません。最大長は 39 文字です。ProgID について詳しくは、「[\<ProgID\> Key](http://msdn.microsoft.com/ja-JP/library/ms690196.aspx.aspx)」をご覧ください。 
  
 _bstrFileSystemDirectoryHint_
  
ローカル ファイルが格納されるディレクトリ ルートを示します。空にすることはできません。最大長は 256 文字です。指定するディレクトリは既に存在していなければなりません。 
  
 _pEventCallback_
  
CsiSyncClient が変更について通知するコールバック インターフェイス。「IPartnerActivityCallback::EventOccurred」をご覧ください。この値は Null にはできません。 
  
 _pfCreatedNewCache_
  
新しいキャッシュが作成されたかどうかを返します。SuppliedID に関連付けられているキャッシュがない場合には、作成されます。この値は Null にはできません。
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |SuppliedID に関連付けられているキャッシュが既に存在しますが、ProgId または FileSystemDirectoryHint が、指定されたものとは異なります。  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (またはサブフォルダー) が別のキャッシュ上に存在します。  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |ProgID が別のキャッシュ上に存在します。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange は、指定のファイルのアップロードを試みるように CsiSyncClient COM オブジェクトに指示する場合に使用します。このメソッドは、ファイルの現在のコンテンツの読み取り操作を含め、ファイルをアップロード用に準備します。アップロードが既に保留中の場合には、以前のアップロードは破棄され、アップロード用に新しいコンテンツが準備されます。対象ファイルが アプリケーションで編集するために開かれている場合、このメソッドによって S_OK が戻され、その場合にはファイルのアップロード準備はなされません (変更がある場合には、アプリケーションが既にこの手順を実行しているはずです)。
  
以前にアップロード ブロック済みとしてマークされていた場合、このメソッドによってアップロードが可能になります ([ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) を参照)。
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>パラメーター

 _bstrFileSystemPath_
  
クライアント上のファイルを示す文字列。この値を空のローカル パスにすることはできません。最大長は 256 文字です。このパスは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)への呼び出しを実行した場合に FileSystemDirectoryHint で指定したディレクトリ ツリー内になければなりません。 
  
 _bstrResourceID_
  
ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。 
  
 _bstrWebPath_
  
サーバー上のファイルを示す文字列。この値は空ではない有効な URL にしなければなりません。ただし、http://support.microsoft.com/kb/208427 で定義されている INTERNET_MAX_URL_LENGTH を超えないようにしてください。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_bstrFileSystemPath_ によって指定されたファイルの ResourceID が、指定されたものと異なります。このエラーが返される場合、種類 LSCEventType_OnFilePathConflict のイベントが送信されます。「 [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)」をご覧ください。  <br/> |
|E_LSC_FILENOTFOUND  <br/> |ファイルが操作中に削除されました。  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |指定されたファイル拡張子は CsiSyncClient COM オブジェクトではサポートされていません。「[ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)」をご覧ください。  <br/> |
|E_LSC_FILEUPTODATE  <br/> |キャッシュ内のファイルにはディスクの最新の変更内容が含まれていたため、COM オブジェクトでアップロードはスケジュールされませんでした。  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |_bstrFileSystemPath_ で指定されたファイルがないか、ロックされています。  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|E_LSC_PATHMISMATCH  <br/> |_bstrResourceID_ で指定されたファイルの FileSystemPath が、指定されたものと異なります。  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |指定されたファイルには別のキャッシュで保留されている変更内容が含まれているため、コンシューマーのキャッシュに関連付けることはできません。  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |指定された WebPath は別のキャッシュに含まれます。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile は、指定の ResourceID に関して新しい URL とローカル パスを関連付けます。ResourceID によって指定されたファイルがキャッシュ内にまだ存在しない場合、作成を試みて、ダウンロードのマークを付けます。
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>パラメーター

 _bstrResourceID_
  
ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。 
  
 _bstrNewFileSystemPath_
  
ファイルの新しいローカル パスを指定する文字列。この値は空ではないローカル パスにする必要があります。最大長は 256 文字です。このパスは、Initialize の呼び出し時に FileSystemDirectoryHint によって指定されたディレクトリ ツリー内になければなりません。 
  
 _bstrNewWebPath_
  
ファイルの新しい URL を指定する文字列。この値は空ではない有効な URL にする必要があります。ただし、http://support.microsoft.com/kb/208427 で定義されている INTERNET_MAX_URL_LENGTH を超えないようにしてください。 
  
 _fBlockUploads_
  
新しい場所へのアップロードが現在許可されているかどうかを示します。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_bstrNewFileSystemPath_ または  _bstrNewWebPath_ がいずれかのキャッシュの別のファイル上に既に存在します。このエラーが返される場合、種類 LSCEventType_OnFilePathConflict のイベントが送信されます。「 [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)」をご覧ください。  <br/> |
|E_LSC_FILENOTFOUND  <br/> |このメソッドの実行中に、キャッシュからファイル情報が削除されました。  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |指定されたファイルが、Office アプリケーションで現在同期されています。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache は、Initialize で指定された SuppliedID と関連付けられているキャッシュを削除します。削除対象にはファイル情報すべても含まれますが、クライアントとサーバー上のファイルはそのまま残ります。また、このメソッドでは、部分的に未初期化状態のオブジェクトもそのままになります。この後の呼び出しで有効なのは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) または [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)のみです。このメソッドは、Initialize が失敗して E_LSC_CACHEMISMATCH が返される場合に呼び出されることがあり、失敗した呼び出しで提供された SuppliedID に関連付けられているキャッシュを削除します。
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>パラメーター

なし
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |呼び出しが失敗しました。  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange は、CsiSyncClient COM オブジェクトに対して、指定されたファイルにダウンロードのマークを付けるように指示します。対象ファイルが Office アプリケーションで編集のために開かれている場合、このメソッドは S_OK を戻し、ファイルにダウンロードのマークは付けません (変更がある場合にはアプリケーションがこの手順を既に実行しているはずです)。
  
このメソッドは、ダウンロードがブロックされているというマークが以前に付けられているダウンロードも実行できます (RenameFile をご覧ください)。
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:-----|:-----|
|bstrFileSystemPath  <br/> |クライアント上のファイルを示す文字列。この値は空ではないローカル パスにする必要があります。最大長は 256 文字です。このパスは、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ツリーになければなりません。  <br/> |
|bstrResourceID  <br/> |ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。  <br/> |
|bstrWebPath  <br/> |サーバー上のファイルを示す文字列。この値は空ではない有効な URL にする必要があります。ただし、http://support.microsoft.com/kb/208427 で定義されているように INTERNET_MAX_URL_LENGTH を超えないようにしてください。  <br/> |
   
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |キャッシュ接続状態を設定できません。  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_bstrFileSystemPath_ によって指定されたファイルの ResourceID が指定されたものと異なります。  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |指定されたファイル拡張子は、CsiSyncClient COM オブジェクトでサポートされていません。「GetSupportedFileExtensions」をご覧ください。  <br/> |
|E_LSC_FILENOTFOUND  <br/> |ファイルが、操作中に削除されました。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|E_LSC_PATHMISMATCH  <br/> |_bstrResourceID_ で指定されたファイルの FileSystemPath が、指定されたものと異なります。  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |指定されたファイルには別のキャッシュで保留中の変更が既に含まれているため、コンシューマーのキャッシュと関連付けることはできません。  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |指定された WebPath は別のキャッシュに含まれます。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

キャッシュをオンライン状態またはオフライン状態に設定します。オフラインの場合、Office は、それぞれのファイルの  _fBlockUploads_ 設定には関係なく、対象キャッシュ内のどのファイルに関してもサーバーとの通信を試みることはありません。 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>パラメーター

 _fIsOnline_
  
キャッシュの接続状態を判別するブール値。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |キャッシュ接続状態を設定できません。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission は、ネットワーク コストおよび電力消費に関して Office の同期ヒューリスティックを上書きまたは復元するときに使用します。3G またはその他の高コストのネットワークの場合、または電源に接続されているのではなくバッテリーで稼働している場合には、適切なときまでネットワーク トラフィックをブロックするように Office で選択することができます。この API のコンシューマーはこれを使用して、Office のヒューリスティックを上書きし、強制同期することが可能です。
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>パラメーター

 _nspType_
  
上書きするコスト ヒューリスティックを定義するフラグ。「[列挙 LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)」をご覧ください。
  
 _fEnableSync_
  
強制同期を有効にしてコスト ヒューリスティックを上書きするか、上書きをしないかを指定します。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |同期ヒューリスティックを上書きできません。  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

COM オブジェクトからキャッシュをアンロードし、終了操作を実行します。COM オブジェクトを破棄する前に、[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)を呼び出す必要があります。呼び出すと、他の API は呼び出すことができず、操作を続行する場合には COM オブジェクトを破棄してから新規作成しなければなりません。 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>パラメーター

なし。
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |初期化前の状態に戻すことができません。  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。  <br/> |
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

このインターフェイスは ILSCEvent イベントのリストを表します。
  
**パブリック メンバー関数**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

イベント一覧から次のイベントを取得します。
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>パラメーター

 _ppiLSCEvent_
  
ILSCEvent インターフェイスへのポインター。
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_FAIL  <br/> |これ以上イベントはありません。  <br/> |
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

最初のイベントに列挙子をリセットします。
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>パラメーター

なし。
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
### <a name="interface-ilscevent"></a>インターフェイス ILSCEvent

このインターフェイスは同期イベントを表します。このインターフェイスから、同期イベントに関するすべての情報を取得できます。
  
**パブリック メンバー関数**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

この値が取り込まれるのは、[ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) が呼び出されるときであり、イベントが作成されたときではないので、現在のファイルのステータスのみを入手できます。競合ステータスが変更された時点でのファイルのステータスではありません。 
  
この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnLocalConflictStateChanged の場合のみです。 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>パラメーター

 _pfIsInConflict_
  
対象イベントに関連付けられているファイルの現在の競合ステータス。
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>パラメーター

 _pnError_
  
このイベントに関連付けられているエラー。
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>パラメーター

 _pbstrETag_
  
このイベントに関連付けられている ETag
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

このイベントの種類を取得します。
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>パラメーター

 _pnEventType_
  
このイベントのイベント種類。有効な値については、「[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)」をご覧ください。null にすることはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

このイベントのローカル作業パスを取得します。
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>パラメーター

 _pbstrLocalWorkingPath_
  
このイベントに関連するファイルのローカル パス。 
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

イベントのリソース ID を取得します。
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>パラメーター

 _pbstrResourceID_
  
このイベントに関連付けられているファイルの ResourceID。
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

この値が取り込まれるのは、イベントの[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnFilePathConflict の場合のみです。 [ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange)、[ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)、[ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) へのいずれかの呼び出しが原因で Office ファイル キャッシュ内の別のファイルと Web パスまたはローカル パスの衝突が生じると、このイベントが生成されます。 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>パラメーター

 _pbstrResourceIDAttempted_
  
このイベントの生成原因となった ResourceID。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>パラメーター

 _pnSyncErrorType_
  
このイベントに関連付けられているエラーの種類。可能性のある値については、「[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)」をご覧ください。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_INVALIDARG  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnFilePathConflict の場合のみです。 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>パラメーター

 _pbstrWebPath_
  
このイベントに関連付けられている Web パスを指定します。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

このインターフェイスは、同期イベントに関する追加情報を保持します。
  
**パブリック メンバー関数**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

同期イベントに関するエラー チェーン情報を取得します。
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>パラメーター

 _pbstrErrorChain_
  
エラー チェーン情報を保持する文字列。Null にはできません。 
  
##### <a name="return-values"></a>戻り値

|値|説明|
|:-----|:-----|
|E_NOTIMPL  <br/> |インストールされているバージョンの Office では、このインターフェイスはサポートされていません。  <br/> |
|E_INVALIDARG  <br/> |1 つ以上のパラメーター値が無効です。  <br/> |
|E_FAIL  <br/> |エラー チェーン情報を利用できません。  <br/> |
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

このインターフェイスは、CSISyncClient COM オブジェクトに対するコールバック関数を提供します。
  
**パブリック メンバー関数**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

これは、CsiSyncClient COM オブジェクトに対して提供されたオブジェクトに対するコールバック関数です。イベントが発生すると (有効なイベント種類については、「[列挙 LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)」を参照)、CsiSyncClient COM オブジェクトがこのメソッドを呼び出して、コンシューマーにシグナル通知することが想定されています。 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>パラメーター

 _eEventTypeOccurred_
  
このイベントのイベント種類。有効値については、「[列挙 LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)」をご覧ください。 
  
##### <a name="return-values"></a>戻り値

必ず S_OK が戻ります。
  
## <a name="enumerations"></a>列挙型

CSISyncClient は次の列挙を使用します。
  
### <a name="enum-lsceventsyncerrortype"></a>列挙 LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

この列挙は、ファイルの同期中に生じる可能性があるエラーのカテゴリを指定します。
  
|列挙子|説明|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |このイベントの同期エラーは想定されていませんでした。特別な考慮が必要になることがあります。既定では、ユーザーによる介入が必要になる可能性があります。  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |このイベントの同期エラーには、特別な考慮は必要ありません。Office によって自動的に処理されます。  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |このイベントの同期エラーはユーザーが解決する必要があります。たとえば、競合エラーをマージするには、ユーザーがドキュメントを開いてマージする必要があります。  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |このイベントの同期エラーはコンシューマーによる介入が必要ですが、ユーザーによる特別な考慮は不要です。  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |このイベントの同期エラーは、コンシューマーが特殊ケースとして介入する必要があります。  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>列挙 LSCEventType
<a name="Enum_LSCEventType"> </a>

この列挙は、特定のファイルで生じる可能性があるイベントの種類を指定します。
  
|列挙子|説明|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |ローカル ファイルに変更が加えられました。  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |ユーザーがファイルを開きました。  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |サーバーからのファイル変更のダウンロードが終了しました。  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |サーバーへのファイル変更のアップロードが終了しました。  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |ファイルのマージ競合状態が変更されました。  <br/> |
|LSCEventType_OnFileAdded  <br/> |ファイルが追加されました。  <br/> |
|LSCEventType_OnFileDeleted  <br/> |ファイルが削除されました。  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |ユーザーのファイルで同期が有効でした。  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |サーバーからのファイル変更のダウンロードが開始されました。  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |サーバーへのファイル変更のアップロードが開始されました。  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |このイベントが生成されるのは、[ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange)、[ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)、[ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) のいずれかへの呼び出しが原因で Office ファイル キャッシュ内の別のファイルと Web パスまたはローカル パスの衝突が生じる場合です。  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>列挙 LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

この列挙は、生じる可能性があるイベントの種類を指定します。コンシューマーは、イベント種類に基づいて特定の ILSCLocalSyncClient 関数を呼び出す必要があります。
  
|列挙子|説明|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |ILSCEvent が生じました。コンシューマーは、[ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)を呼び出してデータを取得しなければなりません。  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |サポート対象ファイル拡張子が変更されました。コンシューマーは、[ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)を呼び出してサポート対象拡張子の新しい一覧を取得しなければなりません。  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>列挙 LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

この列挙は、ネットワーク コスト ヒューリスティックに使用するフラグを指定します。 

|列挙子|説明|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |高コスト (3G など) のネットワークのコスト ヒューリスティックを上書きする場合には True。  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |消費電力のコスト ヒューリスティック (バッテリーなど) を上書きする場合には True。  <br/> |
   
### <a name="enum-lscstatusflag"></a>列挙 LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

この列挙は、ファイルの同期ステータスを表すために使用します。 
  
|列挙子|説明|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |サーバー ファイルへの送信を保留中のデータがある場合には True。  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |サーバー ファイルからのダウンロードを保留中のデータがある場合には True。  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |キャッシュ内のファイルにある Office データが、ディスク上のデータの最新コピーである場合には True。  <br/> |
   

