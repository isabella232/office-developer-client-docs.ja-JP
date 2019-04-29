---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434719"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次に[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出したときに、サービスプロバイダーによって使用されるように設定されたテーブル列セットの有効性をテストします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>パラメーター

 _lpptaCols_
  
> 順番検証するテーブル列を定義するプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した列セットが無効です。 
    
FALSE 
  
> 指定した列セットは有効です。
    
## <a name="remarks"></a>注釈

**FBadColumnSet**関数は、PT_ERROR 型の列を無効として扱い、PT_NULL 型の列を有効なものとして処理します。 
  

