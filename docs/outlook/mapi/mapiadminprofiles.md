---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581287"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイル管理オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]サービスの関数のエントリのオプションを示すフラグのビットマスクです。 
    
 _lppProfAdmin_
  
> [out]新しいプロファイルの管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI では、 **MAPIAdminProfiles**メソッドを使用して、プロファイルの管理オブジェクトを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

