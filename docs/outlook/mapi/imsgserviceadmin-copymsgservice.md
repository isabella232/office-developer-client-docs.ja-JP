---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 95a361a44d4714365b9d8b379a0d7f1cb3f85f27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571690"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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
  
> [in]コピーするメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _lpszDisplayName_
  
> [in]このパラメーターは廃止されました。 
    
 _lpInterfaceToCopy_
  
> [in]コピーするメッセージ サービスのプロファイル セクションにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、標準のプロファイル セクション インターフェイス [IProfSect](iprofsectimapiprop.md)が使用されます。
    
 _lpInterfaceDst_
  
> [in]  _lpObjectDst_ パラメーターが指すオブジェクトにアクセスするために使用するインターフェイスを表す IID へのポインター。 NULL を渡す場合、セッション インターフェイス [IMAPISession](imapisessioniunknown.md)が使用されます。 _lpInterfaceDst_ パラメーターは、このパラメーターにIID_IMsgServiceAdmin。 
    
 _lpObjectDst_
  
> [in]セッションまたはメッセージ サービス管理オブジェクトへのポインター。 オブジェクトの種類は、lpInterfaceDst で渡されるインターフェイス識別子  _に対応する必要があります_。 有効なオブジェクト ポインターは、LPMAPISESSION と LPSERVICEADMIN です。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]メッセージ サービスのコピー方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
SERVICE_UI_ALWAYS 
  
> メッセージ サービスが常に構成プロパティ シートを表示する要求。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービスが正常にコピーされました。
    
MAPI_E_NO_ACCESS 
  
> メッセージ サービスは既にプロファイル内に存在し、それ自体の複数のインスタンスを許可しません。
    
MAPI_E_NOT_FOUND 
  
> **lpUID が** 指す _MAPIUID は_、既存のメッセージ サービスを参照していない。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::CopyMsgService** メソッドは、メッセージ サービスをアクティブ なプロファイルまたは別のプロファイルのどちらかのプロファイルにコピーします。 コピーするメッセージ サービスとコピー先を含むプロファイルは、同じプロファイルである必要は一方で、同じプロファイルである必要は生じ得る。 
  
コピー操作では、メッセージ サービスのエントリ ポイント関数は呼び出されません。 コピーされたメッセージ サービスの構成設定は、元のメッセージ サービスと同じです。 これらの設定を変更するには、クライアントが [IMsgServiceAdmin::ConfigureMsgService メソッドを呼び出す必要](imsgserviceadmin-configuremsgservice.md) があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

