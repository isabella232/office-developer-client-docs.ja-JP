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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418051"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存のセッションのコンテキストで、フォームライブラリプロバイダオブジェクトの[imapiformmgr](imapiformmgriunknown.md)インターフェイスを開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>パラメーター

 _psession_
  
> 順番クライアントアプリケーションによって使用されているセッションへのポインター。
    
 _ppmgr_
  
> 読み上げ返された**imapiformmgr**インターフェイスへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアントアプリケーションが**MAPIOpenFormMgr**関数を呼び出すと、その後のフォーム関連のやり取りは、フォームライブラリプロバイダまたはフォームライブラリプロバイダによって返されるインターフェイスを通じて行われます。 **imapiformmgr**インターフェイスを使用すると、クライアントはメッセージハンドラーを操作し、メッセージクラスとフォームライブラリの間で解決を行うことができます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|フォームマネージャーが開き、フォームを選択できるようになります。  <br/> |CMainDlg:: onselectform  <br/> |mfcmapi は、 **MAPIOpenFormMgr**メソッドを使用してフォームマネージャーを開き、フォームを選択できるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

