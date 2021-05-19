---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427347"
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
  

