---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800596"
---
# <a name="imapimessagesitegetstore"></a>IMAPIMessageSite::GetStore

  
  
**適用対象**: Outlook 
  
このようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。 埋め込まれたメッセージは、メッセージ ・ ストア内で直接の代わりに別のメッセージに格納されている_ppStore_パラメーターでは、このメソッドは NULL を返します。 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a>パラメーター

 _ppStore_
  
> [out]メッセージ ストアへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
S_FALSE 
  
> メッセージを格納しているストアはありません。
    
## <a name="remarks"></a>注釈

フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetStore  <br/> |MFCMAPI 使用可能になる場合に、指定されたストアに現在キャッシュされているポインターを取得する**IMAPIMessageSite::GetStore**メソッドを使用してください。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

