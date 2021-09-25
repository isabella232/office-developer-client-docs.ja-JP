---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16d98d92d825870b566f194ff2815c85c581434d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596219"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーが別のフォーム サーバーを開くのに使用できるフォーム マネージャー インターフェイスを返します。
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a>パラメーター

 _ppFormMgr_
  
> [out]返されるフォーム マネージャー インターフェイスへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFormManager  <br/> |MFCMAPI は **IMAPIMessageSite::GetFormManager** メソッドを使用して [MAPIOpenFormMgr](mapiopenformmgr.md) を呼び出し、その呼び出しの結果を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIOpenFormMgr](mapiopenformmgr.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

