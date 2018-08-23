---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 791dfe094aa0ff1aab656b56fbdf7d59e880b92e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593733"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスをプロファイルにコピーします。 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]コピーするのにはメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpszDisplayName_
  
> [in]このパラメーターは廃止されました。 
    
 _lpInterfaceToCopy_
  
> [in]コピーするのにはメッセージ サービスのプロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すことは、標準のプロファイルで、 [IProfSect](iprofsectimapiprop.md)、使っているインターフェイスになります。
    
 _lpInterfaceDst_
  
> [in]_LpObjectDst_パラメーターが指すオブジェクトへのアクセスに使用するインターフェイスを表す IID へのポインターです。 パラメーターに NULL は、セッション、 [IMAPISession](imapisessioniunknown.md)、使っているインターフェイスになります。 IID_IMsgServiceAdmin に、 _lpInterfaceDst_パラメーターを設定することもできます。 
    
 _lpObjectDst_
  
> [in]セッションまたはメッセージ サービスの管理オブジェクトへのポインターへのポインター。 オブジェクトの種類は、 _lpInterfaceDst_に渡されるインターフェイス識別子に対応します。 有効なオブジェクトのポインターは、LPMAPISESSION および LPSERVICEADMIN です。
    
 _ulUIParam_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。
    
 _ulFlags_
  
> [in]メッセージ サービスをコピーする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
SERVICE_UI_ALWAYS 
  
> 要求をメッセージ サービスは、構成のプロパティ シートを常に表示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービスは正常にコピーされました。
    
MAPI_E_NO_ACCESS 
  
> メッセージ サービスは既にプロファイルに、それ自身の複数のインスタンスを許可しません。
    
MAPI_E_NOT_FOUND 
  
> _LpUID_で示される**MAPIUID**は、既存のメッセージ サービスを参照していません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::CopyMsgService**メソッドは、メッセージ サービスをアクティブなプロファイルまたは別のプロファイル、プロファイルにコピーします。 コピーするメッセージ サービスを含むプロファイルと変換先は、同じプロファイルを使用するはありませんが、ことができます。 
  
コピー操作は、メッセージ サービスのエントリ ポイント関数は呼び出されません。 コピーしたメッセージ サービスには、元のと同じ構成設定があります。 クライアントはこれらの設定を変更するのには、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドを呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

