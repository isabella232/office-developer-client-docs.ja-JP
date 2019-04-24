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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309969"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスをプロファイルにコピーします。 
  
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

 _lpuid_
  
> 順番コピーするメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpszdisplayname_
  
> 順番このパラメーターは推奨されていません。 
    
 _lpInterfaceToCopy_
  
> 順番コピーするメッセージサービスのプロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 標準プロファイルセクションインターフェイス[IProfSect](iprofsectimapiprop.md)で NULL 結果を渡すことができます。
    
 _lpInterfaceDst_
  
> 順番_lpObjectDst_パラメーターによって参照されるオブジェクトへのアクセスに使用されるインターフェイスを表す IID へのポインター。 session インターフェイスの[imapisession](imapisessioniunknown.md)で NULL 結果が渡されています。 _lpInterfaceDst_パラメーターを IID_IMsgServiceAdmin に設定することもできます。 
    
 _lpObjectDst_
  
> 順番session または message service administration オブジェクトへのポインターへのポインター。 オブジェクトの種類は、 _lpInterfaceDst_で渡されるインターフェイス識別子に対応している必要があります。 有効なオブジェクトポインターは、LPMAPISESSION および lpserviceadmin です。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番メッセージサービスのコピー方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
SERVICE_UI_ALWAYS 
  
> メッセージサービスに常に構成プロパティシートが表示されるように要求します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービスが正常にコピーされました。
    
MAPI_E_NO_ACCESS 
  
> メッセージサービスはプロファイルに既に存在し、それ自体の複数のインスタンスを許可しません。
    
MAPI_E_NOT_FOUND 
  
> _lpuid_が指す**MAPIUID**は、既存のメッセージサービスを参照していません。 
    
## <a name="remarks"></a>解説

**IMsgServiceAdmin:: copymsgservice**メソッドは、メッセージサービスをアクティブなプロファイルまたは別のプロファイルのいずれかのプロファイルにコピーします。 コピーするメッセージサービスを含むプロファイルで、宛先は同じプロファイルである必要はありませんが、これを行うことができます。 
  
メッセージサービスのエントリポイント関数は、コピー操作では呼び出されません。 コピーされたメッセージサービスの構成設定は、元のものと同じです。 これらの設定を変更するには、クライアントは[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドを呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

