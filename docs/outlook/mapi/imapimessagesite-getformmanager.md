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
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800602"
---
# <a name="imapimessagesitegetformmanager"></a>IMAPIMessageSite::GetFormManager

  
  
**適用対象**: Outlook 
  
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

