---
title: imapiforminfomakeiconfrombinary
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405115"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのアイコンプロパティの1つからアイコンを作成します。
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>パラメーター

 _npropid_
  
> 順番icon プロパティのプロパティ識別子。
    
 _phicon_
  
> 読み上げ返されるアイコンへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは、 **imapiforminfo:: makeiconfrombinary**メソッドを呼び出して、フォームのアイコンプロパティの1つからアイコンを作成します。 _npropid_パラメーターでは、 **makeiconfrombinary**は、フォームのアイコンプロパティの1つのプロパティ識別子を受け取ります。 このプロパティ識別子を使用すると、アイコンのプロパティ列を含む表ビューに表示できるアイコンが作成されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

