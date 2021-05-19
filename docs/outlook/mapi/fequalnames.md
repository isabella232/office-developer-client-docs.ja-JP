---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414803"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つの MAPI 名前付きプロパティが同じかどうかを決定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>パラメーター

 _lpName1_
  
> [in]最初の名前付 [きプロパティを記述する MAPINAMEID](mapinameid.md) 構造体へのポインター。 
    
 _lpName2_
  
> [in]2 番目の名前付きプロパティを記述する **MAPINAMEID** 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 2 つのプロパティ名は等しくなります。 
    
FALSE 
  
> 2 つのプロパティ名は等しくない。
    
## <a name="remarks"></a>注釈

**FEqualNames** 関数は **、MAPINAMEID** 構造体に [GUID](guid.md)が含まれているため、複数の方法でプロパティ名自体を表す場合に便利です。 つまり、2 つの構造は単純なバイナリ メソッドでは比較できません。 
  
テスト プロセスでは、プロパティ名文字列の大文字と小文字が区別されます。 
  

