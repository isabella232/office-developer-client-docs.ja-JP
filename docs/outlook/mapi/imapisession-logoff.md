---
title: IMAPISessionLogoff
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
ms.openlocfilehash: 7d6ccd64fea0af30e81a2db0bcb9630062b4b64d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800682"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**適用対象**: Outlook 
  
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
  
> [in]ハンドルのダイアログ ボックスの親ウィンドウまたはウィンドウを表示できます。 MAPI_LOGOFF_UI フラグが設定されていない場合、このパラメーターは無視されます。
    
 _ulFlags_
  
> [in]ログオフ操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_LOGOFF_SHARED 
  
> このセッションを共有すると、共有セッションを使用してログオンするすべてのクライアントが実行中のログオフ時の通知する必要があります。 クライアントがログオフする必要があります。 共有セッションを使用している任意のクライアントは、このフラグを設定できます。 MAPI_LOGOFF_SHARED には、現在のセッションが共有されていない場合は無視されます。
    
MAPI_LOGOFF_UI 
  
> **ログオフ**できますダイアログ ボックスを表示、操作中にユーザーに確認を要求する可能性があります。 
    
 _ulReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ログオフ操作が正常に完了しました。
    
## <a name="remarks"></a>注釈

**IMAPISession::Logoff**メソッドでは、MAPI セッションを終了します。 **ログオフ**が返されるときは[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)を除くメソッド呼び出すことができます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ログオフ**が返されるの**** メソッドを呼び出して、セッション オブジェクトを放します。 
  
セッションの終了についての詳細については、 [MAPI セッションを終了](ending-a-mapi-session.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI では、 **IMAPISession::Logoff**メソッドを使用して、それを解放する前にセッションからログオフします。  <br/> |
   
> [!NOTE]
> 、Microsoft Office Outlook 2007 Service Pack 2、Microsoft Outlook 2010 では、および Microsoft Outlook 2013 で導入された高速シャット ダウンの動作のためクライアントは**MAPI_LOGOFF_SHARED**パラメーターを[IMAPISession::Logoff](imapisession-logoff.md)にことはありません渡す必要があります。 **MAPI_LOGOFF_SHARED**を渡すと、すべての MAPI クライアントをシャット ダウンを開始して、予期しない動作が発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI セッションの終了](ending-a-mapi-session.md)

