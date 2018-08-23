---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570129"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームのアイコンのプロパティのいずれかからアイコンを作成します。
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>パラメーター

 _nPropID_
  
> [in]アイコンのプロパティにプロパティの識別子です。
    
 _phicon_
  
> [out]返されるアイコンへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

クライアント アプリケーションは、フォームのアイコンのプロパティのいずれかからアイコンを作成する**IMAPIFormInfo::MakeIconFromBinary**メソッドを呼び出します。 _NPropID_パラメーターには、 **MakeIconFromBinary**は、フォームのアイコンのプロパティのいずれかのプロパティの識別子をかかります。 このプロパティの識別子を使用すると、アイコンのプロパティの列を含む表形式ビューで表示できるアイコンを構築します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

