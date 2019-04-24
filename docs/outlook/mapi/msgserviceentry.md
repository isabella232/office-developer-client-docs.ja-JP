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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341609"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスのエントリポイント関数のプロトタイプを定義して、メッセージサービスの構成をサポートします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|定義された関数の実装:  <br/> |メッセージサービス  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
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
  
> 順番サービスプロバイダー dll のインスタンスのハンドル。 通常、ハンドルはリソースを取得するために使用されます。 
    
 _lpmalloc_
  
> 順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 **IStream**などの特定のインターフェイスを使用する場合、メッセージサービスはこの割り当て方法を使用する必要がある場合があります。 
    
 _lpMAPISup_
  
> 順番[imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスの実装へのポインター。 
    
 _uluiparam_
  
> 順番関数またはゼロにユーザーインターフェイス情報を渡すために使用される実装固有の値。 _uluiparam_パラメーターは、構成ダイアログボックスの親ウィンドウハンドルで、型 HWND (ULONG_PTR へのキャスト) です。 値が0の場合は、親ウィンドウがないことを示します。 
    
 _ulFlags_
  
> 順番サービスエントリ関数のオプションを示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
MSG_SERVICE_UI_READ_ONLY 
  
> サービスの構成ユーザーインターフェイスは現在の構成を表示しますが、ユーザーはそれを変更することはできません。 
    
SERVICE_UI_ALLOWED 
  
> 必要に応じて、構成ダイアログボックスを表示することを許可します。 SERVICE_UI_ALLOWED フラグが設定されている場合、 _lpprops_プロパティの値の配列が空であるか、有効な構成が含まれていない場合にのみ、ダイアログボックスが表示されます。 SERVICE_UI_ALLOWED が設定されていない場合、SERVICE_UI_ALWAYS フラグが設定されている場合は、ダイアログボックスが表示されることがあります。 
    
UI_CURRENT_PROVIDER_FIRST 
  
> 他のダイアログボックスの上に、アクティブなプロバイダーの構成ダイアログボックスが表示されるように要求します。 
    
SERVICE_UI_ALWAYS 
  
> 構成ダイアログボックスを表示するには、メッセージサービスが必要です。 SERVICE_UI_ALWAYS フラグが設定されていない場合でも、SERVICE_UI_ALLOWED フラグが設定されており、有効な構成情報が_lpprops_プロパティ値の配列から利用できない場合は、構成ダイアログボックスが表示されることがあります。 ユーザーインターフェイスを表示できるようにするには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定する必要があります。 
    
 _ulcontext_
  
> 順番MAPI が現在実行している構成操作。 _ulcontext_パラメーターには、次のいずれかの値を格納します。 
    
MSG_SERVICE_CONFIGURE 
  
> サービスの構成の変更は、プロファイルで行う必要があります。 SERVICE_UI_ALWAYS フラグが設定されている場合、サービスはその構成ダイアログボックスを表示する必要があります。 SERVICE_UI_ALLOWED フラグが設定されていて、 _lpprops_パラメーターが空であるか、有効な構成データが含まれていない場合にも、ダイアログボックスが表示されます。 _lpprops_に有効なデータが含まれている場合、ダイアログボックスは表示されず、サービスはこのデータを使用して構成の変更を行う必要があります。 
    
MSG_SERVICE_CREATE 
  
> サービスはプロファイルに追加されています。 SERVICE_UI_ALWAYS または SERVICE_UI_ALLOWED フラグのどちらかが設定されている場合、サービスはその構成ダイアログボックスを表示する必要があります。 どちらのフラグも設定されていない場合、サービスは失敗します。 
    
MSG_SERVICE_DELETE 
  
> サービスがプロファイルから削除されています。 このイベントを受け取った後、サービスは S_OK を返す必要があります。
    
MSG_SERVICE_INSTALL 
  
> サービスは、ネットワーク、フロッピーディスク、またはその他の外部メディアからユーザーのワークステーションにインストールされています。 このイベントを受け取った後、サービスは通常 S_OK を返します。 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> プロバイダーの追加のインスタンスを作成するようにサービスに要求します。 サービスがこの操作をサポートしている場合は、 [IProviderAdmin:: createprovider](iprovideradmin-createprovider.md)を呼び出す必要があります。 サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことができます。 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> プロバイダーインスタンスを削除するようにサービスに要求します。 サービスがこの操作をサポートしている場合は、 [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md)を呼び出す必要があります。 サービスがこの操作をサポートしていない場合は、MAPI_E_NO_SUPPORT を返すことができます。
    
MSG_SERVICE_UNINSTALL 
  
> サービスが削除されています。 このイベントを受け取った後、サービスは、サービスが終了する前に実行する必要があるクリーンアップタスクを実行してから、成功の値を返します。 ユーザーが削除をキャンセルすると、サービスは MAPI_E_USER_CANCEL を返します。 
    
 _cvalues_
  
> 順番_lpprops_パラメーターによって指定された配列内のプロパティ値の数。 MAPI がプロパティ値を渡さない場合、 _cvalues_パラメーターの値は0になります。 
    
 _lpprops_
  
> 順番関数がメッセージサービスを構成するときに使用する、プロバイダーでサポートされているプロパティの値を示す[spropvalue](spropvalue.md)構造のオプションの配列へのポインター。 この関数は、 _ulcontext_パラメーターが MSG_SERVICE_CONFIGURE に設定されている場合にのみ、このパラメーターを使用します。 このパラメーターは、通常、個人用アドレス帳サービスなど、ファイルベースのサービスのファイルへのパスを渡すために使用されます。 MSG_SERVICE_CONFIGURE フラグが_ulflags_パラメーターに渡されていない場合、 _lpprops_パラメーターは0である必要があります。 
    
 _lpprovideradmin_
  
> 順番IProviderAdmin へのポインター [: IUnknown](iprovideradminiunknown.md)インターフェイスは、現在のメッセージサービスの特定のプロバイダーのプロファイルセクションを検索するために使用できます。 
    
 _lppMapiError_
  
> 読み上げ[MAPIERROR](mapierror.md)構造体へのポインター。 この構造体は、 [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して割り当てられます。 すべてのメンバーはオプションですが、ほとんどの構造体には_lpszerror_メンバーに有効なエラーメッセージ文字列が含まれています。 構造体の_lpszcomponent_または_lpszcomponent_メンバーが存在する場合は、基本構造で[MAPIFreeBuffer](mapifreebuffer.md)を1回呼び出すことによって、最終的にメモリを解放する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_UNCONFIGURED 
  
> サービスプロバイダーが構成されていません。 
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
MAPI_E_NO_SUPPORT 
  
> プロバイダーは、オブジェクトへの変更をサポートしていないか、変更の通知をサポートしていません。 
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode がサポートされているかどうか。
    
## <a name="remarks"></a>解説

**msgserviceentry**関数プロトタイプを使用して定義された関数は、メッセージサービスが自分自身を構成したり、その他のサービス固有のアクションを実行したりすることができます。 この関数は、主に、ユーザーがメッセージサービスに固有の設定を変更できるダイアログボックスを furnishes します。 _lpprops_パラメーターで渡されたプロパティ値の配列を使用して、プログラムによる構成をサポートすることもできます。 プログラムによる構成は、サービスが必要なプロファイルウィザードをサポートしていない限り、オプションです。 
  
MAPI は、このエントリポイントをコントロールパネルアプリケーションから呼び出すか、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)または[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出しているクライアントアプリケーションに応答して呼び出します。 
  
MAPI では、メッセージサービスが**msgserviceentry** prototype に使用する関数名に制限はありませんが、name **serviceentry**が優先されます。 関数の序数には制限がありません。1つのプロバイダー DLL に複数の関数を含めることができます。 ただし、 **serviceentry**という名前の関数は1つだけにすることができます。 
  
メッセージサービスでは、 [builddisplaytable](builddisplaytable.md)関数と[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用して、構成ダイアログボックスの実装を簡単にすることができます。 
  
ユーザーは MSG_SERVICE_UNINSTALL 操作を取り消すことができます。 この場合、 **serviceentry**関数は、サービスが削除されないことを確認するためにユーザーに確認し、サービスがインストールされたままの場合は MAPI_E_USER_CANCEL を返します。 
  
**msgserviceentry**プロトタイプに基づく関数は、表示されている HRESULT 値の1つを返します。 MAPI は、 [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)へのクライアントの呼び出しに応答するときにこの値を転送します。 
  
サービスエントリ関数をエクスポートするメッセージサービスには、 **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) および**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のプロパティが含まれている必要があります。MAPISVC.INF。 
  

