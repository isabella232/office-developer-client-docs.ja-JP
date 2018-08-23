---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570493"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a>パラメーター

 _ppFormMgr_
  
> [out]返されるフォーム マネージャーのインターフェイスへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetFormManager  <br/> |MFCMAPI では、 **IMAPIMessageSite::GetFormManager**メソッドを使用して、 [MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出すし、その呼び出しの結果を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIOpenFormMgr](mapiopenformmgr.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

