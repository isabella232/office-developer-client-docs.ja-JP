---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579841"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスを変更する場合、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppServiceAdmin_
  
> [out]メッセージ サービス管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービス管理オブジェクトへのポインターが正常に返されました。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPISession::AdminServices**メソッドは、メッセージ サービスの管理オブジェクト、 **IMsgServiceAdmin**インターフェイスをサポートし、ポインターを返すオブジェクトを作成します。 このポインターを使用すると、セッション ・ プロファイル内のメッセージ サービスのいずれかを変更するのには**IMsgServiceAdmin**メソッドを呼び出すことができます。 これらの変更は反映されません。 次のセッションまでに注意してください。現在のセッションには影響しません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI では、 **IMAPISession::AdminServices**メソッドを使用して、サーバー名を読み取るためのプロファイルにアクセスします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

