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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420592"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
選択ユーティリティ [関数のみを使用している場合は、MAPIInitialize](mapiinitialize.md) を置き換える。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**ScInitMapiUtil** 関数と [DeinitMapiUtil](deinitmapiutil.md)関数は [、MAPIInitialize](mapiinitialize.md)ではなく、選択したユーティリティ関数を呼び出して解放するために協力します。これは、コア関数とユーティリティ関数を呼び出します。 **ScInitMapiUtil がユーティリティ** 関数を呼び出す場合は、必要なメモリも初期化します。 
  
**ScInitMapiUtil** が呼び出した関数の使用が完了したら **、DeinitMapiUtil** を明示的に呼び出して解放する必要があります。 これに対し **、MAPIInitialize は** **DeinitMapiUtil を暗黙的に呼び出します**。 
  
## <a name="see-also"></a>関連項目



[MAPIUninitialize](mapiuninitialize.md)

