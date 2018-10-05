---
title: Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用法について取り上げます。
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399453"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="ae0c9-103">Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用</span><span class="sxs-lookup"><span data-stu-id="ae0c9-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="ae0c9-104">Office ドキュメント キャッシュ (ODC) を制御するための CSISyncClient の使用法について取り上げます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="ae0c9-p101">CSISyncClient はアウトプロセス COM サーバー (CsiSyncClient.exe) で、Microsoft OneDrive はこれを使用して Office ドキュメント キャッシュ (ODC) の動作を制御できます。たとえば、OneDrive は CSISyncClient を介して ODC を呼び出し、MS-FSSHTTP 対応エンドポイントとの間でファイルのアップロードおよびダウンロードを実行することができます。このようにすると、共同編集や、オフラインからオンラインへのシームレスな移行など Office における下位サービス機能を活用できます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p101">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC). For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints. This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="ae0c9-p102">CsiSyncClient は Office デスクトップ (x86 と x64) で利用できます。注: 新しいバージョンの Office には CsiSyncClient が同梱されていますが、このプロセスを使用できるのは下位互換性のために限定されます。ODC を制御するための CsiSyncClient インターフェイスとメソドロジは今後のバージョンの Office で変更される予定です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p102">CsiSyncClient is available in Office Desktop (both x86 and x64). Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only. The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="ae0c9-111">現在、クラス ID は OneDrive にのみ応答するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="ae0c9-p103">COM オブジェクトはアウトプロセス COM サーバーとして使用でき、CsiSyncClient.exe で実行されます。(ODC が使用する) Access の制約のため、Office のビット種類と同じものが、つまり x64 Office では x64 COM オブジェクト、x86 Office では x86 COM オブジェクトがそれぞれ同梱されています。この制約を回避するため、CLSCTX_LOCAL_SERVER を CoCreateInstance の一部として指定すると、アウトプロセス COM サーバーとして COM オブジェクトがホストされ、ビット互換性が確保されます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p103">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe. Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object. To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="ae0c9-115">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ae0c9-115">Interfaces</span></span>

<span data-ttu-id="ae0c9-116">CSISyncClient は以下のインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="ae0c9-117">インターフェイス ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="ae0c9-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="ae0c9-118">これは、Office でファイルを同期するために使用するプライマリ インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="ae0c9-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="ae0c9-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="ae0c9-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="ae0c9-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="ae0c9-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="ae0c9-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="ae0c9-p104">公開されているこの COM オブジェクトはアウトプロセス サーバーとして使用されます。CLSCTX_LOCAL_SERVER を CoCreateInstance の一部として指定すると、64 ビットと 32 ビットのプロセス間で互換性が得られます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p104">The COM object that is exposed is used as an out-of-proc server. Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="ae0c9-p105">COM オブジェクトを共同作成した後、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)を最初に呼び出す必要があります。[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)が正常に完了した後には、任意の API を何度でも希望する順序で呼び出すことができます。また、既に初期化されたオブジェクトで [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)を呼び出すことができますが、呼び出しても何も実行されません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p105">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first. Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order. You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="ae0c9-p106">前述の段落の例外は、[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache)と [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)です。[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)を COM オブジェクトで呼び出した後、このオブジェクトを破棄し、新しいオブジェクトを作成する必要があります。[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache)はサブキャッシュを削除し、そのキャッシュ内のすべての関連ファイル情報を削除しますが、ディスク上のドキュメントはそのままにします。また、キャッシュとの通信のための状態もそのままになります。それにより、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) を再び呼び出して、COM オブジェクトを破棄してから再作成することなく、新しいキャッシュを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p106">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk. It also leaves the state intact for communicating with the cache. This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="ae0c9-132">**パブリック メンバー関数**</span><span class="sxs-lookup"><span data-stu-id="ae0c9-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="ae0c9-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="ae0c9-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="ae0c9-p107">DeleteFile は、キャッシュからファイル情報を削除する場合に使用します。ただし、このメソッドはディスクとサーバー上の関連ファイルはそのままにします。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p107">DeleteFile is used to remove the file information from the cache. However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-136">Parameters</span></span>

 <span data-ttu-id="ae0c9-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae0c9-p108">ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p108">The string which identifies the ResourceID of the file. This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-140">Return values</span></span>

|<span data-ttu-id="ae0c9-141">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-141">Value</span></span>|<span data-ttu-id="ae0c9-142">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-144">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-146">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-148">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae0c9-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae0c9-150">指定された ResourceID がキャッシュにありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-152">これまでに、Initialize が正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-154">現在、ファイルが同期中または開かれた状態であるため、削除できません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-155">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-156">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="ae0c9-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="ae0c9-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="ae0c9-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="ae0c9-p109">GetChanges は ILSCEvent オブジェクトの列挙子を返します。また、GetChanges の次の呼び出しに提供されたトークンも返します。その場合、それまでのイベント セットの処理をコンシューマーが完了したと想定されます。指定された  _nPreviousChangesToken_ より前のイベントは、削除され、使用できません。処理するイベントがない場合、  _pnCurrentChangesToken_ の値は  _nPreviousChangesToken_ と同じになりますが、  _ppiEvents_ は引き続き設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p109">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events. Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable. If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-162">Parameters</span></span>

 <span data-ttu-id="ae0c9-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="ae0c9-164">コンシューマーによって最後に処理されたイベントを示します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="ae0c9-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="ae0c9-p110">コンシューマーに渡された最新のイベントを示します。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p110">Identifies the most recent event being handed to the consumer. Must not be null.</span></span>
  
 <span data-ttu-id="ae0c9-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-168">_ppiEvents_</span></span>
  
<span data-ttu-id="ae0c9-p111">コンシューマーに渡されたイベントの列挙子。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p111">An enumerator for the events handed to the consumer. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-171">Return values</span></span>

|<span data-ttu-id="ae0c9-172">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-172">Value</span></span>|<span data-ttu-id="ae0c9-173">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-175">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-177">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-180">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-181">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="ae0c9-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="ae0c9-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="ae0c9-p112">GetClientNetworkSyncPermission は、ネットワーク コストと消費電力に関する Office の同期ヒューリスティックを上書きするかどうかを照会するときに使用します。3G やその他の高コストのネットワークの場合、または電源に接続されているのではなくバッテリーで稼働している場合には、適切なときまでネットワーク トラフィックをブロックするように Office で選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p112">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden. When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-185">Parameters</span></span>

 <span data-ttu-id="ae0c9-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-186">_nspType_</span></span>
  
<span data-ttu-id="ae0c9-p113">照会対象のコスト ヒューリスティックを定義するフラグ。「[列挙 LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p113">A flag which defines which cost heuristic to query. See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="ae0c9-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="ae0c9-p114">要求されたコスト ヒューリスティックを現在上書きするかどうかを指定します。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p114">Specifies whether the requested cost heuristic is currently overridden or not. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-192">Return values</span></span>

|<span data-ttu-id="ae0c9-193">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-193">Value</span></span>|<span data-ttu-id="ae0c9-194">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-196">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-198">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-201">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-202">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="ae0c9-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="ae0c9-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="ae0c9-p115">GetFileStatus は、特定のファイルに関する情報、つまり、キャッシュ内に存在するかどうか、サーバー コピーとの通信が保留されているかどうか、Office 2013 に含まれているデータがローカル コピーからの最新データかどうかなどの情報を収集するために使用されます。CsiSyncClient COM オブジェクトが照会する情報を判別するには、[列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) 値のビット単位のフラグが必要です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p115">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy. It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-206">Parameters</span></span>

 <span data-ttu-id="ae0c9-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae0c9-p116">クライアント上のファイルを示す文字列。この値を空にすることはできません。最大長は 128 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p116">The string which identifies the file on the client. This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae0c9-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="ae0c9-p117">返す情報を定義するフラグ。「[列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p117">A flag which defines what information to return. See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="ae0c9-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="ae0c9-p118">クライアント上の  _bstrResourceID_ によって識別されるファイルの場所を示す文字列。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p118">The string which identifies the location of the file identified by  _bstrResourceID_ on the client. Must not be null.</span></span> 
  
 <span data-ttu-id="ae0c9-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-216">_pbstrETag_</span></span>
  
<span data-ttu-id="ae0c9-p119">_bstrResourceID_ によって識別されるファイルの eTag が入る文字列。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p119">A string which will contain the eTag for the file identified by  _bstrResourceID_. Must not be null.</span></span> 
  
 <span data-ttu-id="ae0c9-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="ae0c9-p120">_bstrResourceID_ によって識別されるファイルに関して、  _sfRequestedStatus_ を介して要求されるステータスが含まれるフラグ。Null にはできません。「 [列挙 LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)」をご覧くださいい。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p120">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_. Must not be null. See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-223">Return values</span></span>

|<span data-ttu-id="ae0c9-224">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-224">Value</span></span>|<span data-ttu-id="ae0c9-225">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-227">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-229">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae0c9-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae0c9-231">_bstrResourceID_ によって指定されたファイル情報がキャッシュ内にありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="ae0c9-233">LSCStatusFlag_LocalFileUnchanged が要求されたか、 _bstrResourceID_ によって指定されたファイルがロックされているか、または存在しません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-236">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-237">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="ae0c9-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="ae0c9-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="ae0c9-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="ae0c9-p121">GetSupportedFileExtensions は、現在 CsiSyncClient COM オブジェクトによってサポートされているパイプ区切りファイル拡張子の一覧を返します。この一覧は変更される可能性があります。コンシューマーは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)で提供される IPartnerActivityCallback オブジェクトを介して変更を通知されます (EventOccured をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p121">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object. Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="ae0c9-242">戻される文字列の例: "|docx|docm|pptx|"</span><span class="sxs-lookup"><span data-stu-id="ae0c9-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-243">Parameters</span></span>

 <span data-ttu-id="ae0c9-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="ae0c9-p122">CsiSyncClient COM オブジェクトによってサポートされているファイル拡張子のパイプ区切りセットで設定する文字列。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p122">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-247">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-247">Return values</span></span>

|<span data-ttu-id="ae0c9-248">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-248">Value</span></span>|<span data-ttu-id="ae0c9-249">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-251">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-253">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-256">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-257">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="ae0c9-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="ae0c9-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="ae0c9-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="ae0c9-p123">呼び出される最初のメソッドは、Initialize でなければなりません。そうでない場合には、他のすべての API は E_LSC_NOTINITIALIZED を返します。既に初期化されたオブジェクトで Initialize を呼び出すと、S_OK が戻り、何も実行されません。E_LSC_CACHEMISMATCH が戻る場合には、呼び出し側は [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) を呼び出して、指定の SuppliedID と関連付けられているキャッシュを削除できます。ただし、その場合には他の API では E_LSC_NOTINITIALIZED がやはり戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p123">Initialize must be the first method called. Otherwise, all other APIs will return E_LSC_NOTINITIALIZED. Calling Initialize on an already initialized object returns S_OK and does nothing. If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID. However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-265">Parameters</span></span>

 <span data-ttu-id="ae0c9-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="ae0c9-p124">コンシューマー、および使用するキャッシュを示します。空にすることはできず、最大長は 32 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p124">Identifies the consumer and which cache to use. Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="ae0c9-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-269">_bstrProgID_</span></span>
  
<span data-ttu-id="ae0c9-p125">双方向通信のためのコンシューマーの COM オブジェクトを示します。空にすることはできません。最大長は 39 文字です。ProgID の詳細については、「[\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p125">Identifies the consumer's COM object for two-way communication. Must be non-empty with a maximum of 39 characters. See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="ae0c9-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="ae0c9-p126">ローカル ファイルが格納されるディレクトリ ルートを示します。空にすることはできません。最大長は 256 文字です。指定するディレクトリは既に存在していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p126">Identifies the directory root in which local files will be stored. Must be non-empty with a maximum of 256 characters. The directory must already exist.</span></span> 
  
 <span data-ttu-id="ae0c9-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-277">_pEventCallback_</span></span>
  
<span data-ttu-id="ae0c9-p127">CsiSyncClient が変更について通知するコールバック インターフェイス。「IPartnerActivityCallback::EventOccurred」をご覧ください。この値は Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p127">The callback interface which CsiSyncClient will notify on changes. See IPartnerActivityCallback::EventOccurred. This value must not be null.</span></span> 
  
 <span data-ttu-id="ae0c9-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="ae0c9-p128">新しいキャッシュが作成されたかどうかを返します。SuppliedID に関連付けられているキャッシュがない場合には、作成されます。この値は Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p128">Returns whether a new cache was created. If no cache is associated with the SuppliedID, one will be created. This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-285">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-285">Return values</span></span>

|<span data-ttu-id="ae0c9-286">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-286">Value</span></span>|<span data-ttu-id="ae0c9-287">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-289">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-291">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae0c9-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="ae0c9-293">SuppliedID に関連付けられているキャッシュが既に存在しますが、ProgId または FileSystemDirectoryHint が、指定されたものとは異なります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="ae0c9-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="ae0c9-295">FileSystemDirectoryHint (またはサブフォルダー) が別のキャッシュ上に存在します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="ae0c9-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="ae0c9-297">ProgID が別のキャッシュ上に存在します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-298">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-299">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="ae0c9-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="ae0c9-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="ae0c9-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="ae0c9-p129">LocalFileChange は、指定のファイルのアップロードを試みるように CsiSyncClient COM オブジェクトに指示する場合に使用します。このメソッドは、ファイルの現在のコンテンツの読み取り操作を含め、ファイルをアップロード用に準備します。アップロードが既に保留中の場合には、以前のアップロードは破棄され、アップロード用に新しいコンテンツが準備されます。対象ファイルが アプリケーションで編集するために開かれている場合、このメソッドによって S_OK が戻され、その場合にはファイルのアップロード準備はなされません (変更がある場合には、アプリケーションが既にこの手順を実行しているはずです)。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p129">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file. The method will prepare the file for upload, including reading the file's current contents. If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload. If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="ae0c9-306">以前にアップロード ブロック済みとしてマークされていた場合、このメソッドによってアップロードが可能になります ([ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) を参照)。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-307">Parameters</span></span>

 <span data-ttu-id="ae0c9-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="ae0c9-p130">クライアント上のファイルを示す文字列。この値を空のローカル パスにすることはできません。最大長は 256 文字です。このパスは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)への呼び出しを実行した場合に FileSystemDirectoryHint で指定したディレクトリ ツリー内になければなりません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p130">A string which identifies the file on the client. This value must be a non-empty local path with a maximum of 256 characters. This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="ae0c9-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae0c9-p131">ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p131">A string which identifies the ResourceID of the file. This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae0c9-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="ae0c9-p132">サーバー上のファイルを示す文字列。この値は空ではない有効な URL にしなければなりません。ただし、https://support.microsoft.com/kb/208427 で定義されている INTERNET_MAX_URL_LENGTH を超えないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p132">A string which identifies the file on the server. This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-318">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-318">Return values</span></span>

|<span data-ttu-id="ae0c9-319">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-319">Value</span></span>|<span data-ttu-id="ae0c9-320">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-322">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-324">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae0c9-p133">_bstrFileSystemPath_ によって指定されたファイルの ResourceID が、指定されたものと異なります。このエラーが返される場合、種類 LSCEventType_OnFilePathConflict のイベントが送信されます。「 [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)」をご覧ください。  </span><span class="sxs-lookup"><span data-stu-id="ae0c9-p133">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified. An event of type LSCEventType_OnFilePathConflict is sent when this error is returned. See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  </span></span><br/> |
|<span data-ttu-id="ae0c9-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae0c9-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae0c9-330">ファイルが操作中に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="ae0c9-p134">指定されたファイル拡張子は CsiSyncClient COM オブジェクトではサポートされていません。「[ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)」をご覧ください。  </span><span class="sxs-lookup"><span data-stu-id="ae0c9-p134">The given file extension is not supported by the CsiSyncClient COM object. See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  </span></span><br/> |
|<span data-ttu-id="ae0c9-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="ae0c9-335">キャッシュ内のファイルにはディスクの最新の変更内容が含まれていたため、COM オブジェクトでアップロードはスケジュールされませんでした。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="ae0c9-337">_bstrFileSystemPath_ で指定されたファイルがないか、ロックされています。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae0c9-339">指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae0c9-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="ae0c9-343">_bstrResourceID_ で指定されたファイルの FileSystemPath が、指定されたものと異なります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-345">指定されたファイルには別のキャッシュで保留されている変更内容が含まれているため、コンシューマーのキャッシュに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-347">指定された WebPath は別のキャッシュに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-348">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-349">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="ae0c9-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="ae0c9-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="ae0c9-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="ae0c9-p135">RenameFile は、指定の ResourceID に関して新しい URL とローカル パスを関連付けます。ResourceID によって指定されたファイルがキャッシュ内にまだ存在しない場合、作成を試みて、ダウンロードのマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p135">RenameFile will associate a new URL and local path for a given ResourceID. If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-354">Parameters</span></span>

 <span data-ttu-id="ae0c9-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae0c9-p136">ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p136">A string which identifies the ResourceID of the file. This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae0c9-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="ae0c9-p137">ファイルの新しいローカル パスを指定する文字列。この値は空ではないローカル パスにする必要があります。最大長は 256 文字です。このパスは、Initialize の呼び出し時に FileSystemDirectoryHint によって指定されたディレクトリ ツリー内になければなりません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p137">A string which specifies the new local path for the file. This value must be a non-empty local path with a maximum of 256 characters. This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="ae0c9-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="ae0c9-p138">ファイルの新しい URL を指定する文字列。この値は空ではない有効な URL にする必要があります。ただし、https://support.microsoft.com/kb/208427 で定義されている INTERNET_MAX_URL_LENGTH を超えないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p138">A string which specifies the new URL for the file. This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="ae0c9-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="ae0c9-366">新しい場所へのアップロードが現在許可されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-367">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-367">Return values</span></span>

|<span data-ttu-id="ae0c9-368">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-368">Value</span></span>|<span data-ttu-id="ae0c9-369">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-371">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-373">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae0c9-p139">_bstrNewFileSystemPath_ または  _bstrNewWebPath_ がいずれかのキャッシュの別のファイル上に既に存在します。このエラーが返される場合、種類 LSCEventType_OnFilePathConflict のイベントが送信されます。「 [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)」をご覧ください。  </span><span class="sxs-lookup"><span data-stu-id="ae0c9-p139">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache. An event of type LSCEventType_OnFilePathConflict is sent when this error is returned. See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  </span></span><br/> |
|<span data-ttu-id="ae0c9-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae0c9-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae0c9-379">このメソッドの実行中に、キャッシュからファイル情報が削除されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae0c9-381">指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-385">指定されたファイルが、Office アプリケーションで現在同期されています。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-386">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-387">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="ae0c9-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="ae0c9-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="ae0c9-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="ae0c9-p140">ResetCache は、Initialize で指定された SuppliedID と関連付けられているキャッシュを削除します。削除対象にはファイル情報すべても含まれますが、クライアントとサーバー上のファイルはそのまま残ります。また、このメソッドでは、部分的に未初期化状態のオブジェクトもそのままになります。この後の呼び出しで有効なのは、[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) または [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)のみです。このメソッドは、Initialize が失敗して E_LSC_CACHEMISMATCH が返される場合に呼び出されることがあり、失敗した呼び出しで提供された SuppliedID に関連付けられているキャッシュを削除します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p140">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize. This includes all of the file information, but will leave the files on both the client and the server. This method also leaves the object in a partially uninitialized state. The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-395">Parameters</span></span>

<span data-ttu-id="ae0c9-396">なし</span><span class="sxs-lookup"><span data-stu-id="ae0c9-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-397">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-397">Return values</span></span>

|<span data-ttu-id="ae0c9-398">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-398">Value</span></span>|<span data-ttu-id="ae0c9-399">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-401">呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-404">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-405">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="ae0c9-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="ae0c9-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="ae0c9-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae0c9-p141">ServerFileChange は、CsiSyncClient COM オブジェクトに対して、指定されたファイルにダウンロードのマークを付けるように指示します。対象ファイルが Office アプリケーションで編集のために開かれている場合、このメソッドは S_OK を戻し、ファイルにダウンロードのマークは付けません (変更がある場合にはアプリケーションがこの手順を既に実行しているはずです)。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p141">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download. If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="ae0c9-410">このメソッドは、ダウンロードがブロックされているというマークが以前に付けられているダウンロードも実行できます (RenameFile をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-411">Parameters</span></span>

|<span data-ttu-id="ae0c9-412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-412">Parameter</span></span>|<span data-ttu-id="ae0c9-413">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="ae0c9-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="ae0c9-p142">クライアント上のファイルを示す文字列。この値は空ではないローカル パスにする必要があります。最大長は 256 文字です。このパスは、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ツリーになければなりません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p142">A string which identifies the file on the client. This value must be a non-empty local path with a maximum of 256 characters. This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="ae0c9-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="ae0c9-p143">ファイルの ResourceID を示す文字列。この値を空にすることはできません。最大長は 128 文字です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p143">A string which identifies the ResourceID of the file. This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="ae0c9-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="ae0c9-p144">サーバー上のファイルを示す文字列。この値は空ではない有効な URL にする必要があります。ただし、https://support.microsoft.com/kb/208427 で定義されているように INTERNET_MAX_URL_LENGTH を超えないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p144">A string which identifies the file on the server. This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="ae0c9-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-424">Return values</span></span>

|<span data-ttu-id="ae0c9-425">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-425">Value</span></span>|<span data-ttu-id="ae0c9-426">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-428">キャッシュ接続状態を設定できません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae0c9-430">_bstrFileSystemPath_ によって指定されたファイルの ResourceID が指定されたものと異なります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="ae0c9-p145">指定されたファイル拡張子は、CsiSyncClient COM オブジェクトでサポートされていません。「GetSupportedFileExtensions」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p145">The given file extension is not supported by the CsiSyncClient COM object. See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae0c9-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae0c9-435">ファイルが、操作中に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-437">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae0c9-439">指定の FileSystemPath が、Initialize の呼び出し時に FileSystemDirectoryHint で指定されたディレクトリ ルートにありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae0c9-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="ae0c9-443">_bstrResourceID_ で指定されたファイルの FileSystemPath が、指定されたものと異なります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-445">指定されたファイルには別のキャッシュで保留中の変更が既に含まれているため、コンシューマーのキャッシュと関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="ae0c9-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="ae0c9-447">指定された WebPath は別のキャッシュに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-448">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-449">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="ae0c9-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="ae0c9-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="ae0c9-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae0c9-p146">キャッシュをオンライン状態またはオフライン状態に設定します。オフラインの場合、Office は、それぞれのファイルの  _fBlockUploads_ 設定には関係なく、対象キャッシュ内のどのファイルに関してもサーバーとの通信を試みることはありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p146">Sets the cache into an online or offline state. If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-454">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-454">Parameters</span></span>

 <span data-ttu-id="ae0c9-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-455">_fIsOnline_</span></span>
  
<span data-ttu-id="ae0c9-456">キャッシュの接続状態を判別するブール値。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-457">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-457">Return values</span></span>

|<span data-ttu-id="ae0c9-458">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-458">Value</span></span>|<span data-ttu-id="ae0c9-459">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-461">キャッシュ接続状態を設定できません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-463">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-466">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-467">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="ae0c9-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="ae0c9-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="ae0c9-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae0c9-p147">SetClientNetworkSyncPermission は、ネットワーク コストおよび電力消費に関して Office の同期ヒューリスティックを上書きまたは復元するときに使用します。3G またはその他の高コストのネットワークの場合、または電源に接続されているのではなくバッテリーで稼働している場合には、適切なときまでネットワーク トラフィックをブロックするように Office で選択することができます。この API のコンシューマーはこれを使用して、Office のヒューリスティックを上書きし、強制同期することが可能です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p147">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage. When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time. The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-473">Parameters</span></span>

 <span data-ttu-id="ae0c9-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-474">_nspType_</span></span>
  
<span data-ttu-id="ae0c9-p148">上書きするコスト ヒューリスティックを定義するフラグ。「[列挙 LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p148">A flag which defines which cost heuristic to override. See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="ae0c9-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-477">_fEnableSync_</span></span>
  
<span data-ttu-id="ae0c9-478">強制同期を有効にしてコスト ヒューリスティックを上書きするか、上書きをしないかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-479">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-479">Return values</span></span>

|<span data-ttu-id="ae0c9-480">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-480">Value</span></span>|<span data-ttu-id="ae0c9-481">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-483">同期ヒューリスティックを上書きできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-486">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-487">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="ae0c9-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="ae0c9-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="ae0c9-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="ae0c9-p149">COM オブジェクトからキャッシュをアンロードし、終了操作を実行します。COM オブジェクトを破棄する前に、[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)を呼び出す必要があります。呼び出すと、他の API は呼び出すことができず、操作を続行する場合には COM オブジェクトを破棄してから新規作成しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p149">Unloads the cache from the COM object and perform closing operations. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object. Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-493">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-493">Parameters</span></span>

<span data-ttu-id="ae0c9-494">なし。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-495">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-495">Return values</span></span>

|<span data-ttu-id="ae0c9-496">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-496">Value</span></span>|<span data-ttu-id="ae0c9-497">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-499">初期化前の状態に戻すことができません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae0c9-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae0c9-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)がこれまでに正常に呼び出されなかったことがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-502">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-503">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="ae0c9-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="ae0c9-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="ae0c9-505">このインターフェイスは ILSCEvent イベントのリストを表します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="ae0c9-506">**パブリック メンバー関数**</span><span class="sxs-lookup"><span data-stu-id="ae0c9-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="ae0c9-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="ae0c9-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="ae0c9-508">イベント一覧から次のイベントを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-509">Parameters</span></span>

 <span data-ttu-id="ae0c9-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="ae0c9-511">ILSCEvent インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-512">Return values</span></span>

|<span data-ttu-id="ae0c9-513">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-513">Value</span></span>|<span data-ttu-id="ae0c9-514">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-516">これ以上イベントはありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-517">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-518">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="ae0c9-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="ae0c9-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="ae0c9-520">最初のイベントに列挙子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-521">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-521">Parameters</span></span>

<span data-ttu-id="ae0c9-522">なし。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-523">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-523">Return values</span></span>

<span data-ttu-id="ae0c9-524">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="ae0c9-525">インターフェイス ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="ae0c9-525">Interface ILSCEvent</span></span>

<span data-ttu-id="ae0c9-p150">このインターフェイスは同期イベントを表します。このインターフェイスから、同期イベントに関するすべての情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p150">This interface represents a synchronizing event. All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="ae0c9-528">**パブリック メンバー関数**</span><span class="sxs-lookup"><span data-stu-id="ae0c9-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="ae0c9-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="ae0c9-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="ae0c9-530">この値が取り込まれるのは、[ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) が呼び出されるときであり、イベントが作成されたときではないので、現在のファイルのステータスのみを入手できます。競合ステータスが変更された時点でのファイルのステータスではありません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="ae0c9-531">この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnLocalConflictStateChanged の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-532">Parameters</span></span>

 <span data-ttu-id="ae0c9-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="ae0c9-534">対象イベントに関連付けられているファイルの現在の競合ステータス。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-535">Return values</span></span>

<span data-ttu-id="ae0c9-536">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="ae0c9-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="ae0c9-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="ae0c9-538">この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-539">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-539">Parameters</span></span>

 <span data-ttu-id="ae0c9-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-540">_pnError_</span></span>
  
<span data-ttu-id="ae0c9-541">このイベントに関連付けられているエラー。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-542">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-542">Return values</span></span>

<span data-ttu-id="ae0c9-543">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="ae0c9-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="ae0c9-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="ae0c9-545">この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-546">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-546">Parameters</span></span>

 <span data-ttu-id="ae0c9-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-547">_pbstrETag_</span></span>
  
<span data-ttu-id="ae0c9-548">このイベントに関連付けられている ETag</span><span class="sxs-lookup"><span data-stu-id="ae0c9-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-549">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-549">Return values</span></span>

<span data-ttu-id="ae0c9-550">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="ae0c9-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="ae0c9-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="ae0c9-552">このイベントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-553">Parameters</span></span>

 <span data-ttu-id="ae0c9-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-554">_pnEventType_</span></span>
  
<span data-ttu-id="ae0c9-p151">このイベントのイベント種類。有効な値については、「[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)」をご覧ください。null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p151">The event type of this event. See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-558">Return values</span></span>

|<span data-ttu-id="ae0c9-559">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-559">Value</span></span>|<span data-ttu-id="ae0c9-560">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-562">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-563">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-564">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="ae0c9-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="ae0c9-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="ae0c9-566">このイベントのローカル作業パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-567">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-567">Parameters</span></span>

 <span data-ttu-id="ae0c9-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="ae0c9-569">このイベントに関連するファイルのローカル パス。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-570">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-570">Return values</span></span>

<span data-ttu-id="ae0c9-571">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="ae0c9-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="ae0c9-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="ae0c9-573">イベントのリソース ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-574">Parameters</span></span>

 <span data-ttu-id="ae0c9-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="ae0c9-576">このイベントに関連付けられているファイルの ResourceID。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-577">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-577">Return values</span></span>

<span data-ttu-id="ae0c9-578">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="ae0c9-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="ae0c9-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="ae0c9-p152">この値が取り込まれるのは、イベントの[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnFilePathConflict の場合のみです。 [ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange)、[ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)、[ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) へのいずれかの呼び出しが原因で Office ファイル キャッシュ内の別のファイルと Web パスまたはローカル パスの衝突が生じると、このイベントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p152">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict. When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-582">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-582">Parameters</span></span>

 <span data-ttu-id="ae0c9-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="ae0c9-p153">このイベントの生成原因となった ResourceID。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p153">The ResourceID that caused this event to get generated. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-586">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-586">Return values</span></span>

<span data-ttu-id="ae0c9-587">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="ae0c9-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="ae0c9-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="ae0c9-589">この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnServerChangesDownloaded または LSCEventType_OnLocalChangesUploaded の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-590">Parameters</span></span>

 <span data-ttu-id="ae0c9-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="ae0c9-p154">このイベントに関連付けられているエラーの種類。可能性のある値については、「[列挙 LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)」をご覧ください。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p154">The error type associated with this event. See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-595">Return values</span></span>

|<span data-ttu-id="ae0c9-596">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-596">Value</span></span>|<span data-ttu-id="ae0c9-597">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-599">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-600">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-601">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="ae0c9-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="ae0c9-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="ae0c9-603">この値が取り込まれるのは、イベントの [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) が LSCEventType_OnFilePathConflict の場合のみです。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-604">Parameters</span></span>

 <span data-ttu-id="ae0c9-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="ae0c9-p155">このイベントに関連付けられている Web パスを指定します。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p155">Specifies the Web Path associated with this event. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-608">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-608">Return values</span></span>

<span data-ttu-id="ae0c9-609">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="ae0c9-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="ae0c9-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="ae0c9-611">このインターフェイスは、同期イベントに関する追加情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="ae0c9-612">**パブリック メンバー関数**</span><span class="sxs-lookup"><span data-stu-id="ae0c9-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="ae0c9-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="ae0c9-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="ae0c9-614">同期イベントに関するエラー チェーン情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-615">Parameters</span></span>

 <span data-ttu-id="ae0c9-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="ae0c9-p156">エラー チェーン情報を保持する文字列。Null にはできません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p156">A string to hold the error chain information. Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-619">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-619">Return values</span></span>

|<span data-ttu-id="ae0c9-620">値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-620">Value</span></span>|<span data-ttu-id="ae0c9-621">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="ae0c9-623">インストールされているバージョンの Office では、このインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="ae0c9-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae0c9-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae0c9-625">1 つ以上のパラメーター値が無効です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae0c9-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae0c9-627">エラー チェーン情報を利用できません。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae0c9-628">S_OK</span></span>  <br/> |<span data-ttu-id="ae0c9-629">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="ae0c9-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="ae0c9-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="ae0c9-631">このインターフェイスは、CSISyncClient COM オブジェクトに対するコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="ae0c9-632">**パブリック メンバー関数**</span><span class="sxs-lookup"><span data-stu-id="ae0c9-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="ae0c9-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="ae0c9-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="ae0c9-p157">これは、CsiSyncClient COM オブジェクトに対して提供されたオブジェクトに対するコールバック関数です。イベントが発生すると (有効なイベント種類については、「[列挙 LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)」を参照)、CsiSyncClient COM オブジェクトがこのメソッドを呼び出して、コンシューマーにシグナル通知することが想定されています。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p157">This is a callback function on the object given to the CsiSyncClient COM object. It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="ae0c9-636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae0c9-636">Parameters</span></span>

 <span data-ttu-id="ae0c9-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="ae0c9-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="ae0c9-p158">このイベントのイベント種類。有効値については、「[列挙 LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p158">The event type of this event. See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae0c9-640">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae0c9-640">Return values</span></span>

<span data-ttu-id="ae0c9-641">必ず S_OK が戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="ae0c9-642">列挙型</span><span class="sxs-lookup"><span data-stu-id="ae0c9-642">Enumerations</span></span>

<span data-ttu-id="ae0c9-643">CSISyncClient は次の列挙を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="ae0c9-644">列挙 LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="ae0c9-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="ae0c9-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="ae0c9-646">この列挙は、ファイルの同期中に生じる可能性があるエラーのカテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="ae0c9-647">列挙子</span><span class="sxs-lookup"><span data-stu-id="ae0c9-647">Enumerator</span></span>|<span data-ttu-id="ae0c9-648">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="ae0c9-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="ae0c9-p159">このイベントの同期エラーは想定されていませんでした。特別な考慮が必要になることがあります。既定では、ユーザーによる介入が必要になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p159">The synchronizing error of this event was unexpected, and may require special consideration. By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae0c9-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae0c9-p160">このイベントの同期エラーには、特別な考慮は必要ありません。Office によって自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p160">The synchronizing error of this event does not need special consideration. Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae0c9-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae0c9-p161">このイベントの同期エラーはユーザーが解決する必要があります。たとえば、競合エラーをマージするには、ユーザーがドキュメントを開いてマージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p161">The synchronizing error of this event requires a user to resolve it. For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="ae0c9-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="ae0c9-659">このイベントの同期エラーはコンシューマーによる介入が必要ですが、ユーザーによる特別な考慮は不要です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae0c9-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae0c9-661">このイベントの同期エラーは、コンシューマーが特殊ケースとして介入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="ae0c9-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="ae0c9-663">列挙 LSCEventType</span><span class="sxs-lookup"><span data-stu-id="ae0c9-663">Enum LSCEventType</span></span>
<span data-ttu-id="ae0c9-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="ae0c9-665">この列挙は、特定のファイルで生じる可能性があるイベントの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="ae0c9-666">列挙子</span><span class="sxs-lookup"><span data-stu-id="ae0c9-666">Enumerator</span></span>|<span data-ttu-id="ae0c9-667">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="ae0c9-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="ae0c9-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="ae0c9-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="ae0c9-670">ローカル ファイルに変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="ae0c9-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="ae0c9-672">ユーザーがファイルを開きました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="ae0c9-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="ae0c9-674">サーバーからのファイル変更のダウンロードが終了しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="ae0c9-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="ae0c9-676">サーバーへのファイル変更のアップロードが終了しました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="ae0c9-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="ae0c9-678">ファイルのマージ競合状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="ae0c9-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="ae0c9-680">ファイルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="ae0c9-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="ae0c9-682">ファイルが削除されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="ae0c9-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="ae0c9-684">ユーザーのファイルで同期が有効でした。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="ae0c9-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="ae0c9-686">サーバーからのファイル変更のダウンロードが開始されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="ae0c9-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="ae0c9-688">サーバーへのファイル変更のアップロードが開始されました。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="ae0c9-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="ae0c9-690">このイベントが生成されるのは、[ILSCLocalSyncClient::LocalFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange)、[ILSCLocalSyncClient::ServerFileChange](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)、[ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) のいずれかへの呼び出しが原因で Office ファイル キャッシュ内の別のファイルと Web パスまたはローカル パスの衝突が生じる場合です。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="ae0c9-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="ae0c9-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="ae0c9-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="ae0c9-693">列挙 LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="ae0c9-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="ae0c9-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="ae0c9-p162">この列挙は、生じる可能性があるイベントの種類を指定します。コンシューマーは、イベント種類に基づいて特定の ILSCLocalSyncClient 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-p162">This enumeration specifies the type of events that can occur. The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="ae0c9-697">列挙子</span><span class="sxs-lookup"><span data-stu-id="ae0c9-697">Enumerator</span></span>|<span data-ttu-id="ae0c9-698">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="ae0c9-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="ae0c9-p163">ILSCEvent が生じました。コンシューマーは、[ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)を呼び出してデータを取得しなければなりません。  </span><span class="sxs-lookup"><span data-stu-id="ae0c9-p163">An ILSCEvent has occurred. The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.  </span></span><br/> |
|<span data-ttu-id="ae0c9-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="ae0c9-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="ae0c9-p164">サポート対象ファイル拡張子が変更されました。コンシューマーは、[ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)を呼び出してサポート対象拡張子の新しい一覧を取得しなければなりません。  </span><span class="sxs-lookup"><span data-stu-id="ae0c9-p164">The supported file extensions have changed. The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.  </span></span><br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="ae0c9-705">列挙 LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="ae0c9-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="ae0c9-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="ae0c9-707">この列挙は、ネットワーク コスト ヒューリスティックに使用するフラグを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="ae0c9-708">列挙子</span><span class="sxs-lookup"><span data-stu-id="ae0c9-708">Enumerator</span></span>|<span data-ttu-id="ae0c9-709">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="ae0c9-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="ae0c9-711">高コスト (3G など) のネットワークのコスト ヒューリスティックを上書きする場合には True。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="ae0c9-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="ae0c9-713">消費電力のコスト ヒューリスティック (バッテリーなど) を上書きする場合には True。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="ae0c9-714">列挙 LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="ae0c9-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="ae0c9-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="ae0c9-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="ae0c9-716">この列挙は、ファイルの同期ステータスを表すために使用します。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="ae0c9-717">列挙子</span><span class="sxs-lookup"><span data-stu-id="ae0c9-717">Enumerator</span></span>|<span data-ttu-id="ae0c9-718">説明</span><span class="sxs-lookup"><span data-stu-id="ae0c9-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae0c9-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="ae0c9-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="ae0c9-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="ae0c9-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="ae0c9-721">サーバー ファイルへの送信を保留中のデータがある場合には True。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="ae0c9-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="ae0c9-723">サーバー ファイルからのダウンロードを保留中のデータがある場合には True。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="ae0c9-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="ae0c9-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="ae0c9-725">キャッシュ内のファイルにある Office データが、ディスク上のデータの最新コピーである場合には True。</span><span class="sxs-lookup"><span data-stu-id="ae0c9-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

