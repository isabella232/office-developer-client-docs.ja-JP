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
  
フォームのいずれかのアイコン プロパティからアイコンを作成します。
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>パラメーター

 _nPropID_
  
> [in]icon プロパティのプロパティ識別子。
    
 _phicon_
  
> [out]返されるアイコンへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormInfo::MakeIconFromBinary** メソッドを呼び出して、フォームのアイコン プロパティの 1 つからアイコンを作成します。 _nPropID パラメーターで_**、MakeIconFromBinary は** フォームのアイコン プロパティの 1 つのプロパティ識別子を取得します。 このプロパティ識別子を使用すると、アイコンのプロパティ列を含むテーブル ビューに表示できるアイコンが作成されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

