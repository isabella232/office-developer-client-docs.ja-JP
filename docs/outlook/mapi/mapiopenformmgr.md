---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586033"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
既存のセッションのコンテキストでは、フォーム ライブラリのプロバイダー オブジェクトの[IMAPIFormMgr](imapiformmgriunknown.md)インターフェイスを開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>パラメーター

 _pSession_
  
> [in]クライアント アプリケーションによって使用中のセッションへのポインター。
    
 _ppmgr_
  
> [out]返される**IMAPIFormMgr**インターフェイスへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアント アプリケーションを**MAPIOpenFormMgr**関数の呼び出しを行った後のほとんどのフォームに関連する操作が行わフォーム ライブラリ プロバイダーまたはフォーム ライブラリ プロバイダーによって返されるインターフェイスを使用します。 **IMAPIFormMgr**インターフェイスは、メッセージ ハンドラーを使用し、メッセージ クラスとフォーム ライブラリの間での解決策を実行するクライアントを使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp は、フォームを選択できるように、フォーム マネージャーを開きます。  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI では、 **MAPIOpenFormMgr**メソッドを使用して、フォームを選択できるように、フォーム マネージャーを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

