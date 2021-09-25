---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70d6365ed2f1b38da7759c4d872c25358dc927d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556813"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ScInitMapiUtil](scinitmapiutil.md)関数によって明示的に、または[MAPIInitialize](mapiinitialize.md)関数によって暗黙的に呼び出されるユーティリティ関数を解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>パラメーター

なし 
  
## <a name="return-value"></a>戻り値

なし 
  
## <a name="remarks"></a>注釈

**DeinitMapiUtil 関数は**[、ScInitMapiUtil](scinitmapiutil.md)または [MAPIInitialize で初期化された関数を解放します](mapiinitialize.md)。 
  
**ScInitMapiUtil** によって呼び出される関数の使用が完了したら **、DeinitMapiUtil** を明示的に呼び出して解放する必要があります。 これに対し [、MAPIUninitialize は](mapiuninitialize.md) **DeinitMapiUtil を暗黙的に呼び出します**。 
  

