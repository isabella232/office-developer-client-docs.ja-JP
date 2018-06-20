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
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800542"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**適用されます**: Outlook 
  
フォームのアイコンのプロパティのいずれかからアイコンを作成します。
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parameters

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



[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)

