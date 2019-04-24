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
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351262"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
select ユーティリティ関数のみが使用されている場合は、 [MAPIInitialize](mapiinitialize.md)を置き換えます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
    
## <a name="remarks"></a>解説

**ScInitMapiUtil**および[DeinitMapiUtil](deinitmapiutil.md)関数は、連携して、コアとユーティリティ関数を呼び出す[MAPIInitialize](mapiinitialize.md)ではなく、選択ユーティリティ関数を呼び出しおよび解放します。 **ScInitMapiUtil**がユーティリティ関数を呼び出すと、必要なメモリも初期化されます。 
  
**ScInitMapiUtil**が呼び出された関数の使用が完了したら、 **DeinitMapiUtil**を明示的に呼び出して解放する必要があります。 これに対して、 **MAPIInitialize**は暗黙的に**DeinitMapiUtil**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[MAPIUninitialize](mapiuninitialize.md)

