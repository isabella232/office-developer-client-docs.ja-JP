---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270148"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカルフォームライブラリへのインターフェイスポインターを返します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _ppfcnt_
  
> 読み上げローカルフォームライブラリのインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

ポインターが返されるインターフェイスは、サードパーティのインストールプログラムによって使用され、アプリケーション固有のフォームをプログラムが MAPI にログオンすることなく、ライブラリにインストールできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: OnMAPIOpenLocalFormContainer  <br/> |mfcmapi は、 **MAPIOpenLocalFormContainer**メソッドを使用して、ローカルフォームコンテナーを開き、新しいウィンドウにレンダリングします。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

