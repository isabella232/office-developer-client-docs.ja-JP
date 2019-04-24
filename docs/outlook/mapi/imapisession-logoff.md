---
title: imapisessionlogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338109"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI セッションを終了します。
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番表示されるダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 MAPI_LOGOFF_UI フラグが設定されていない場合、このパラメーターは無視されます。
    
 _ulFlags_
  
> 順番ログオフ操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_LOGOFF_SHARED 
  
> このセッションが共有されている場合、共有セッションを使用してログオンしたすべてのクライアントに、進行中のログオフが通知されます。 クライアントはログオフする必要があります。 共有セッションを使用しているクライアントは、このフラグを設定できます。 現在のセッションが共有されていない場合、MAPI_LOGOFF_SHARED は無視されます。
    
MAPI_LOGOFF_UI 
  
> **ログオフ**操作中にダイアログボックスを表示することができます。ユーザーに確認を求めるメッセージが表示される可能性があります。 
    
 _ulreserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフ操作が正常に完了しました。
    
## <a name="remarks"></a>解説

**imapisession:: Logoff**メソッドは MAPI セッションを終了します。 **Logoff**が戻ると、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を除くすべてのメソッドを呼び出すことができなくなります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ログオフ**時に、 **IUnknown:: release**メソッドを呼び出して session オブジェクトを解放します。 
  
セッションを終了する方法の詳細については、「 [MAPI セッションを終了する](ending-a-mapi-session.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects  <br/> |cmapiobjects:: Logoff  <br/> |mfcmapi は、 **imapisession:: Logoff**メソッドを使用してセッションからログオフしてから、セッションを解放します。  <br/> |
   
> [!NOTE]
> microsoft Office Outlook 2007 Service Pack 2、microsoft outlook 2010、および microsoft outlook 2013 で導入された高速シャットダウンの動作により、クライアントは**MAPI_LOGOFF_SHARED**パラメーターを[imapisession:: LOGOFF](imapisession-logoff.md)に渡すことはできません。 **MAPI_LOGOFF_SHARED**を渡すと、すべての MAPI クライアントがシャットダウンを開始し、予期しない動作が発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI セッションの終了](ending-a-mapi-session.md)

