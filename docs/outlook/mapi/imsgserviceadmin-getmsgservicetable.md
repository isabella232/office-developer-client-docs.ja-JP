---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 368c32374e47dd97dce54980c566ac14f78c75ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620717"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のメッセージ サービスの一覧であるメッセージ サービス テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]常に NULL。
    
 _lppTable_
  
> [out]メッセージ サービス テーブルへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービス テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::GetMsgServiceTable** メソッドは、セッション プロファイルに現在インストールされているメッセージ サービスを一覧表示する MAPI が保持するテーブルであるメッセージ サービス テーブルへのアクセスを提供します。 メッセージ サービス テーブルの列の完全な一覧については [、「Message Service Table」を参照してください](message-service-tables.md)。
  
メッセージ サービス テーブルは静的です。 クライアントにアクセス権が与えられた後、それ以降のメッセージ サービスの追加または削除は、そのクライアントに影響を与えかねない。 現在のプロファイルにメッセージ サービスがない場合 **、GetMsgServiceTable** は行が 0 のテーブルを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI は **、IMsgServiceAdmin::GetMsgServiceTable** メソッドを使用して、ビューでレンダリングするプロファイル内のサービス テーブルを読み込む。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

