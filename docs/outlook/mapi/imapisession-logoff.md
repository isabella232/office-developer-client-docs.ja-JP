---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e808f573608a8ba822f0fa8942b2cbfab82b421b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592418"
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

 _ulUIParam_
  
> [in]表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 このパラメーターは、フラグが設定されていないMAPI_LOGOFF_UI無視されます。
    
 _ulFlags_
  
> [in]ログオフ操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_LOGOFF_SHARED 
  
> このセッションが共有されている場合は、共有セッションを使用してログオンしたすべてのクライアントに、進行中のログオフが通知されます。 クライアントはログオフする必要があります。 共有セッションを使用しているクライアントは、このフラグを設定できます。 MAPI_LOGOFF_SHAREDセッションが共有されていない場合、この値は無視されます。
    
MAPI_LOGOFF_UI 
  
> **ログオフ** では、操作中にダイアログ ボックスを表示し、ユーザーに確認を求めるメッセージが表示される場合があります。 
    
 _ulReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフ操作が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISession::Logoff メソッドは** MAPI セッションを終了します。 **Logoff が返** された場合 [、IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)以外のメソッドは呼び出されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**Logoff が返** された場合は、その **IUnknown::Release** メソッドを呼び出してセッション オブジェクトを解放します。 
  
セッションの終了の詳細については、「MAPI セッションの [終了」を参照してください](ending-a-mapi-session.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI は **IMAPISession::Logoff** メソッドを使用して、セッションを解放する前にセッションからログオフします。  <br/> |
   
> [!NOTE]
> Microsoft Office Outlook 2007 Service Pack 2、Microsoft Outlook 2010、および Microsoft Outlook 2013 で導入された高速シャットダウン動作のため、クライアントは **MAPI_LOGOFF_SHARED** パラメーターを [IMAPISession::Logoff](imapisession-logoff.md)に渡す必要はありません。 この **MAPI_LOGOFF_SHARED** すると、すべての MAPI クライアントがシャットダウンを開始し、予期しない動作が発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI セッションの終了](ending-a-mapi-session.md)

