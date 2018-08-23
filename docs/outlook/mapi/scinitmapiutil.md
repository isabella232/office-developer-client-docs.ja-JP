---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803824"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**適用対象**: Outlook 
  
[ユーティリティ関数だけを使用する場合に[生じます](mapiinitialize.md)を置き換えます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

[生じます](mapiinitialize.md)コアとユーティリティを呼び出すのではなく、機能の選択のユーティリティ関数を解放し、 **ScInitMapiUtil**および[DeinitMapiUtil](deinitmapiutil.md)関数が協力します。 **ScInitMapiUtil**では、ユーティリティ関数を呼び出すと、も、必要なメモリを初期化します。 
  
**ScInitMapiUtil**が呼び出されている関数の使用が完了すると、それらを解放する**DeinitMapiUtil**を明示的に呼び出す必要があります。 **生じます**は対照的に、 **DeinitMapiUtil**を暗黙的に呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIUninitialize](mapiuninitialize.md)

