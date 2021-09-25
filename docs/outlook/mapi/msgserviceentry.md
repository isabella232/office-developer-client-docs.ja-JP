---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8cfd9e655a9690ac2207a36849fe1b6c63d99719
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575359"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスの構成をサポートするメッセージ サービス エントリ ポイント関数のプロトタイプを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |メッセージ サービス  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>パラメーター

 _hInstance_
  
> [in]サービス プロバイダーDLL のインスタンスのハンドル。 ハンドルは通常、リソースの取得に使用されます。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 メッセージ サービスは、IStream などの特定のインターフェイスを操作するときに、この割り当て方法を使用する **必要がある場合があります**。 
    
 _lpMAPISup_
  
> [in] [IMAPISupport へのポインター : IUnknown インターフェイス](imapisupportiunknown.md) の実装。 
    
 _ulUIParam_
  
> [in]ユーザー インターフェイス情報を関数または 0 に渡す場合に使用される実装固有の値。 _ulUIParam_ パラメーターは、構成ダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型 (ULONG_PTR。 値が 0 の場合は、親ウィンドウが表示されません。 
    
 _ulFlags_
  
> [in]サービス エントリ関数のオプションを示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
MSG_SERVICE_UI_READ_ONLY 
  
> サービスの構成ユーザー インターフェイスは、現在の構成を表示する必要がありますが、ユーザーが変更を許可しない必要があります。 
    
SERVICE_UI_ALLOWED 
  
> 必要に応じて、構成ダイアログ ボックスを表示できます。 SERVICE_UI_ALLOWEDフラグを設定すると  _、lpProps_ プロパティ値配列が空か、有効な構成が含まれている場合にのみ、ダイアログ ボックスが表示されます。 このSERVICE_UI_ALLOWED設定されていない場合、このフラグが設定されている場合は、SERVICE_UI_ALWAYS表示される場合があります。 
    
UI_CURRENT_PROVIDER_FIRST 
  
> アクティブなプロバイダーの構成ダイアログ ボックスを他のダイアログ ボックスの上に表示する要求。 
    
SERVICE_UI_ALWAYS 
  
> 構成ダイアログ ボックスを表示するには、メッセージ サービスが必要です。 SERVICE_UI_ALWAYS フラグが設定されていない場合、SERVICE_UI_ALLOWED フラグが設定され、有効な構成情報が  _lpProps_ プロパティ値配列から使用できない場合は、構成ダイアログ ボックスが表示される場合があります。 ユーザー SERVICE_UI_ALLOWED表示SERVICE_UI_ALWAYSを許可するには、ユーザー インターフェイスまたはユーザー インターフェイスを設定する必要があります。 
    
 _ulContext_
  
> [in]MAPI が現在実行している構成操作。 _ulContext パラメーター_ には、次のいずれかの値が含まれます。 
    
MSG_SERVICE_CONFIGURE 
  
> サービスの構成に対する変更は、プロファイルで行う必要があります。 このフラグSERVICE_UI_ALWAYS設定されている場合、サービスは構成ダイアログ ボックスを表示する必要があります。 このダイアログ ボックスは、SERVICE_UI_ALLOWED フラグが設定され  _、lpProps_ パラメーターが空の場合、または有効な構成データが含まれている場合にも表示されます。 _lpProps に有効_ なデータが含まれている場合は、ダイアログ ボックスを表示し、サービスは構成を変更するためにこのデータを使用する必要があります。 
    
MSG_SERVICE_CREATE 
  
> サービスがプロファイルに追加されています。 サービスの構成SERVICE_UI_ALWAYSまたはSERVICE_UI_ALLOWEDが設定されている場合、サービスは構成ダイアログ ボックスを表示する必要があります。 どちらのフラグも設定しない場合、サービスは失敗します。 
    
MSG_SERVICE_DELETE 
  
> サービスはプロファイルから削除されています。 このイベントを受け取った後、サービスはイベントをS_OK。
    
MSG_SERVICE_INSTALL 
  
> サービスは、ネットワーク、フロッピー ディスク、または他の外部メディアからユーザーのワークステーションにインストールされています。 このイベントを受け取った後、サービスは通常、S_OK。 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> サービスがプロバイダーの追加インスタンスを作成する要求。 サービスがこの操作をサポートしている場合は [、IProviderAdmin::CreateProvider を呼び出す必要があります](iprovideradmin-createprovider.md)。 サービスがこの操作をサポートしていない場合は、この操作をMAPI_E_NO_SUPPORT。 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> サービスがプロバイダー インスタンスを削除する要求。 サービスがこの操作をサポートしている場合は [、IProviderAdmin::D eleteProvider を呼び出す必要があります](iprovideradmin-deleteprovider.md)。 サービスがこの操作をサポートしていない場合は、この操作をMAPI_E_NO_SUPPORT。
    
MSG_SERVICE_UNINSTALL 
  
> サービスが削除されています。 このイベントを受け取った後、サービスは、サービスが終了する前に実行する必要があるすべてのクリーンアップ タスクを実行し、成功した値で戻ります。 ユーザーが削除を取り消した場合、サービスは削除をMAPI_E_USER_CANCEL。 
    
 _cValues_
  
> [in]  _lpProps_ パラメーターが指す配列内のプロパティ値の数。 MAPI がプロパティ値を渡す場合  _、cValues_ パラメーターの値は 0 です。 
    
 _lpProps_
  
> [in]メッセージ サービスの構成で関数が使用するプロバイダーがサポートするプロパティの値を示す [SPropValue](spropvalue.md) 構造体の省略可能な配列へのポインター。 この関数は  _、ulContext_ パラメーターがパラメーターに設定されている場合にのみ、このパラメーターをMSG_SERVICE_CONFIGURE。 このパラメーターは、通常、個人用アドレス帳サービスなどのファイル ベースのサービスのファイルにパスを渡す場合に使用されます。 _ulFlags_ パラメーター MSG_SERVICE_CONFIGUREフラグが渡されない場合 _、lpProps_ パラメーターは 0 である必要があります。 
    
 _lpProviderAdmin_
  
> [in]現在のメッセージ サービス内の特定のプロバイダーのプロファイル セクションを検索するために関数が使用できる [IProviderAdmin:IUnknown](iprovideradminiunknown.md) インターフェイスへのポインター。 
    
 _lppMapiError_
  
> [out] [MAPIERROR 構造体への](mapierror.md) ポインター。 この構造体は [、MAPIAllocateBuffer 関数で割り当](mapiallocatebuffer.md) てされます。 ほとんどの構造体には  _lpszError_ メンバーに有効なエラー メッセージ文字列が含まれますが、すべてのメンバーは省略可能です。 構造体の  _lpszComponent_ メンバーまたは  _lpszError_ メンバーが存在する場合、基本構造の [MAPIFreeBuffer](mapifreebuffer.md) を 1 回呼び出してメモリを解放する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_UNCONFIGURED 
  
> サービス プロバイダーが構成されていません。 
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
MAPI_E_NO_SUPPORT 
  
> プロバイダーは、オブジェクトの変更をサポートしないか、変更の通知をサポートしていません。 
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定MAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**MSGSERVICEENTRY** 関数プロトタイプを使用して定義された関数を使用すると、メッセージ サービスは自分自身を構成したり、他のサービス固有のアクションを実行したりできます。 この関数は、主に、ユーザーがメッセージ サービスに固有の設定を変更できるダイアログ ボックスを提供します。 lpProps パラメーターで渡されたプロパティ値配列を使用して、プログラムによる構成  _をサポート_ することもできます。 プログラムによる構成は、必要なプロファイル ウィザードがサービスでサポートされていない限り、オプションです。 
  
MAPI は、コントロール パネル アプリケーションから、または [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) または [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すクライアント アプリケーションに応答して、このエントリ ポイントを呼び出します。 
  
MAPI は、メッセージ サービスが **MSGSERVICEENTRY** プロトタイプに使用する関数名に制限を設定しませんが **、ServiceEntry** という名前を優先します。 関数の序数に制限はありません。また、1 つのプロバイダー DLL に複数の関数を含めできます。 ただし、ServiceEntry という名前の関数は **1 つのみです**。 
  
メッセージ サービスは [、BuildDisplayTable](builddisplaytable.md) 関数と [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) メソッドを使用して、構成ダイアログ ボックスの実装を簡略化できます。 
  
ユーザーがユーザー操作をキャンセルMSG_SERVICE_UNINSTALLできます。 この場合 **、ServiceEntry** 関数はユーザーに確認して、サービスを削除し、サービスがインストールされたままMAPI_E_USER_CANCELを返す必要があります。 
  
**MSGSERVICEENTRY プロトタイプに基づく** 関数は、一覧表示されている HRESULT 値のいずれかを返します。 MAPI は、クライアントの呼び出しに応答するときにこの値を [IMsgServiceAdmin::ConfigureMsgService に転送します](imsgserviceadmin-configuremsgservice.md)。 
  
サービス エントリ関数をエクスポートするメッセージ サービスには **、MAPISVC.INF** のメッセージ サービス セクションに PR_SERVICE_DLL_NAME ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) プロパティと **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) プロパティが含まれる必要があります。 
  

