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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574798"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ユーティリティ関数が明示的に呼び出される[ScInitMapiUtil](scinitmapiutil.md)関数によって、暗黙的に[生じます](mapiinitialize.md)を解放します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>パラメーター

なし 
  
## <a name="return-value"></a>戻り値

なし 
  
## <a name="remarks"></a>注釈

**DeinitMapiUtil**関数は、 [ScInitMapiUtil](scinitmapiutil.md)または[生じます](mapiinitialize.md)を使用して初期化関数を解放します。 
  
**ScInitMapiUtil**によって呼び出される関数の使用が完了すると、それらを解放する**DeinitMapiUtil**を明示的に呼び出す必要があります。 [MAPIUninitialize](mapiuninitialize.md)は対照的に、 **DeinitMapiUtil**を暗黙的に呼び出します。 
  

