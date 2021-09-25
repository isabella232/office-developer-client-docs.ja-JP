---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 813c76d2c4d81dd50760fc356c2af6f8cc41054e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567586"
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

