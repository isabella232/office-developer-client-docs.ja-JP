---
title: imapisessionadminservices
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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322415"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスに変更を加えるための[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppserviceadmin_
  
> 読み上げメッセージサービス管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービス管理オブジェクトへのポインターが正常に返されました。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**imapisession:: adminservices**メソッドは、 **IMsgServiceAdmin**インターフェイスをサポートするオブジェクトであるメッセージサービス管理オブジェクトを作成し、ポインターを返します。 このポインターを使用すると、 **IMsgServiceAdmin**メソッドを呼び出して、セッションプロファイル内の任意のメッセージサービスを変更できます。 これらの変更は、次のセッションが終了するまで有効にならないことに注意してください。現在のセッションは影響を受けません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIStoreFunctions  <br/> |getservername  <br/> |mfcmapi は、 **imapisession:: adminservices**メソッドを使用して、プロファイルにアクセスしてサーバー名を読み取ります。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

