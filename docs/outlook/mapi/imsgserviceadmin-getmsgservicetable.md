---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309976"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービステーブル (プロファイル内のメッセージサービスのリスト) へのアクセスを提供します。
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番常に NULL。
    
 _lpptable_
  
> 読み上げメッセージサービステーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービステーブルが正常に返されました。
    
## <a name="remarks"></a>解説

**IMsgServiceAdmin:: getmsgservicetable**メソッドは、メッセージサービステーブルへのアクセスを提供します。これは、MAPI が管理するテーブルで、セッションプロファイルに現在インストールされているメッセージサービスを一覧表示します。 メッセージサービステーブルの列の完全な一覧については、「 [message service table](message-service-tables.md)」を参照してください。
  
メッセージサービステーブルは静的です。 クライアントがアクセス権を付与されると、それ以降のメッセージサービスの追加または削除によって影響を受けることはありません。 現在のプロファイルにメッセージサービスがない場合、 **getmsgservicetable**は0行のテーブルを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg  <br/> |CMsgServiceTableDlg:: onrefreshview  <br/> |mfcmapi は、 **IMsgServiceAdmin:: getmsgservicetable**メソッドを使用して、ビューに表示するサービスの表をプロファイルに読み込みます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

