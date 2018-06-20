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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801024"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**適用されます**: Outlook 
  
メッセージ サービス テーブルで、[プロファイルのメッセージ サービスの一覧へのアクセスを提供します。
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]常に NULL を返します。
    
 _lppTable_
  
> [out]メッセージ サービス テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービス テーブルは正常に返されました。
    
## <a name="remarks"></a>備考

**IMsgServiceAdmin::GetMsgServiceTable**メソッドは、メッセージ サービス テーブルで、セッション ・ プロファイルに現在インストールされているメッセージ サービスを一覧表示する MAPI を保持するテーブルへのアクセスを提供します。 メッセージ サービス テーブル内の列の一覧については、[メッセージ サービス テーブル](message-service-tables.md)を参照してください。
  
メッセージ サービス テーブルは静的です。 クライアント アクセスが許可されたことを後、それ以降のメッセージ サービスの追加または削除しないに影響します。 現在のプロファイルでサービスのメッセージがない場合、 **GetMsgServiceTable**は、0 個の行を持つテーブルを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI では、 **IMsgServiceAdmin::GetMsgServiceTable**メソッドを使用して、ビューに表示するプロファイル内のサービスのテーブルをロードします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

