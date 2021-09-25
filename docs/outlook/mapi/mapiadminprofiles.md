---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2ff33145b5a1358f12cbccebc79a60a96953d32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584090"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル管理オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]サービス エントリ関数のオプションを示すフラグのビットマスク。 
    
 _lppProfAdmin_
  
> [out]新しいプロファイル管理オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI は **MAPIAdminProfiles メソッドを使用して** プロファイル管理オブジェクトを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

