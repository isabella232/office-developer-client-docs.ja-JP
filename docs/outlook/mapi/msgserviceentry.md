---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801673"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**適用されます**: Outlook 
  
メッセージ サービスの構成をサポートするメッセージ サービスのエントリ ポイント関数のプロトタイプを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装される関数の定義:  <br/> |メッセージ サービス  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in]サービス providerDLL のインスタンスのハンドル。 ハンドルは通常、リソースを取得するために使用されます。 
    
 _lpMalloc_
  
> [in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 メッセージ サービスは、 **IStream**などの特定のインターフェイスを使用する場合、この割り当て方法を使用する必要があります。 
    
 _lpMAPISup_
  
> [in]ポインター、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インターフェイスの実装です。 
    
 _ulUIParam_
  
> [in]関数にユーザー インターフェイスの情報を渡すための実装に固有の値です。 _UlUIParam_パラメーターの構成] ダイアログ ボックスの親ウィンドウのハンドル、HWND 型にキャスト、ULONG_PTR) の種類の。 0 の値は、親ウィンドウがないことを示します。 
    
 _ulFlags_
  
> [in]サービスの関数のエントリのオプションを示すフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
MSG_SERVICE_UI_READ_ONLY 
  
> サービスの構成のユーザー インターフェイスは現在の構成を表示する必要がありますが、それを変更するユーザーを許可しません。 
    
SERVICE_UI_ALLOWED 
  
> 必要な場合に表示される、[構成] ダイアログ ボックスを許可します。 SERVICE_UI_ALLOWED フラグを設定すると、 _lpProps_プロパティの値の配列が空または無効な構成が含まれていない場合にのみ、ダイアログ ボックスが表示されます。 SERVICE_UI_ALLOWED が設定されていない場合、SERVICE_UI_ALWAYS フラグが設定されている場合、ダイアログ ボックスが表示されますも可能性があります。 
    
UI_CURRENT_PROVIDER_FIRST 
  
> その他のダイアログ ボックスの上にアクティブなプロバイダーの構成] ダイアログ ボックスを表示するように要求します。 
    
SERVICE_UI_ALWAYS 
  
> メッセージ サービスの構成] ダイアログ ボックスを表示する必要があります。 SERVICE_UI_ALWAYS フラグが設定されていない場合、SERVICE_UI_ALLOWED フラグが設定されていて有効な構成情報は、 _lpProps_プロパティの値の配列から、[構成] ダイアログ ボックスが表示されますも可能性があります。 ユーザー インターフェイスを表示するを許可するには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定しなければなりません。 
    
 _ulContext_
  
> [in]MAPI を現在実行している構成の処理。 _UlContext_パラメーターは、次の値のいずれかに含まれます。 
    
MSG_SERVICE_CONFIGURE 
  
> サービスの構成には、プロファイルに変更する必要があります。 SERVICE_UI_ALWAYS フラグが設定されている場合、サービスは、[構成] ダイアログ ボックスに表示されます。 ダイアログ ボックスは、SERVICE_UI_ALLOWED フラグが設定されており、 _lpProps_パラメーターが空か、無効な構成データが含まれていない場合にも表示されます。 _LpProps_に有効なデータが含まれている場合は、ダイアログ ボックスを表示する必要があり、サービスは、構成の変更を行うためこのデータを使用する必要があります。 
    
MSG_SERVICE_CREATE 
  
> サービスは、プロファイルに追加されます。 SERVICE_UI_ALWAYS または SERVICE_UI_ALLOWED のいずれかのフラグが設定されている場合、サービスは、[構成] ダイアログ ボックスに表示されます。 どちらのフラグが設定されている場合、サービスが失敗する必要があります。 
    
MSG_SERVICE_DELETE 
  
> プロファイルからサービスを削除しています。 このイベントを受け取ると、サービスは、S_OK を返す必要があります。
    
MSG_SERVICE_INSTALL 
  
> サービスは、ネットワーク、フロッピー ディスク、またはその他の外部メディアからユーザーのワークステーションにインストールされました。 このイベントを受信した後、サービスは、通常、S_OK を返します。 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> サービスがプロバイダーの追加のインスタンスを作成することを要求します。 サービスは、この操作をサポートする場合は、 [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)をに呼び出す必要があります。 サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことです。 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> サービスがプロバイダーのインスタンスを削除することを要求します。 サービスは、この操作をサポートする場合は、 [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md)をに呼び出す必要があります。 サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことです。
    
MSG_SERVICE_UNINSTALL 
  
> サービスを削除しています。 このイベントを受信した後、サービスはサービスを終了し、成功した場合の値を返す前に行う必要があります任意のクリーンアップ タスクを実行できます。 ユーザーは、削除をキャンセルした場合、サービスは、MAPI_E_USER_CANCEL を返す必要があります。 
    
 _あう_
  
> [in]_LpProps_パラメーターが指す配列内のプロパティ値の数です。 _あう_パラメーターの値は、プロパティの値を渡すことは、MAPI がない場合は 0 です。 
    
 _lpProps_
  
> [in][SPropValue](spropvalue.md)の省略可能な配列へのポインターでは、メッセージ サービスを構成する際にこの関数を使用するプロバイダーでサポートされているプロパティの値を示す構造体します。 関数は、 _ulContext_パラメーターを MSG_SERVICE_CONFIGURE に設定されている場合にだけこのパラメーターを使用します。 このパラメーターは、個人用アドレス帳サービスなどのファイル ・ ベースのサービスのファイルへのパスを渡すに通常使用されます。 _UlFlags_パラメーターに MSG_SERVICE_CONFIGURE フラグが渡されない場合、 _lpProps_パラメーターは 0 にする必要があります。 
    
 _lpProviderAdmin_
  
> [in]関数は、現在のメッセージ サービスで特定のプロバイダーのプロファイル セクションを検索に使用できる[IProviderAdmin:IUnknown](iprovideradminiunknown.md)インターフェイスへのポインター。 
    
 _lppMapiError_
  
> [out][MAPIERROR](mapierror.md)構造体へのポインター。 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数では、構造体が割り当てられます。 ほとんどの構造体は_lpszError_のメンバーで有効なエラー メッセージ文字列を含むすべてのメンバーはオプションですが。 構造体の_lpszComponent_または_lpszError_のメンバーが存在する場合は、基本構造に[MAPIFreeBuffer](mapifreebuffer.md)を 1 回の呼び出しによって、メモリを解放最終的にする必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_UNCONFIGURED 
  
> サービス プロバイダーが構成されていません。 
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
MAPI_E_NO_SUPPORT 
  
> プロバイダーは、そのオブジェクトへの変更をサポートしていないか、または変更の通知をサポートしていません。 
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装には、Unicode のみサポートしています。
    
## <a name="remarks"></a>備考

**MSGSERVICEENTRY**関数のプロトタイプを使用して定義された関数は、それ自体を構成するのにはまたはその他のサービスに固有のアクションを実行するのには、メッセージ サービスを使用できます。 関数は、主にユーザーがメッセージ サービスに固有の設定を変更できるダイアログ ボックスを提供します。 _LpProps_パラメーターで渡されたプロパティ値の配列を使用して、プログラムによる構成もサポートできます。 プログラムによる構成は、サービスがサポートするプロファイル ウィザードでは、することが必要な場合を除き、省略可能です。 
  
MAPI は、コントロール パネルのアプリケーションまたは[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)または[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すクライアント アプリケーションへの応答として、このエントリ ポイントを呼び出します。 
  
MAPI でないを配置制限関数の名前をメッセージ サービス**MSGSERVICEENTRY**のプロトタイプを使用してですが、 **ServiceEntry**の名前を希望します。 関数の序数に制限はありませんし、1 つのプロバイダー DLL が 1 つ以上の関数を含めることができます。 ただし、関数の 1 つだけに**ServiceEntry**を付けることができます。 
  
メッセージ サービスでは、構成ダイアログ ボックスの実装を簡略化するのに、 [BuildDisplayTable](builddisplaytable.md)関数、および[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用できます。 
  
MSG_SERVICE_UNINSTALL 操作をキャンセルするのにはユーザーのことができます。 この例では、 **ServiceEntry**関数では、ユーザーがサービスを削除することはできませんし、サービスがインストールされている場合は、MAPI_E_USER_CANCEL を返すことを確認して確認してください。 
  
**MSGSERVICEENTRY**プロトタイプでは関数では、HRESULT の値のいずれかを返します。 MAPI は、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)へのクライアントの呼び出しに応答する場合にこの値を転送します。 
  
サービス エントリ関数をエクスポートするメッセージ サービスは、メッセージ サービスのセクションで、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) と**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のプロパティを含める必要があります。MAPISVC.INF。 
  

