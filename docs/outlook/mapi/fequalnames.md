---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 51052bd3ee46e880f84cbc0fd5ace69f2ae68f21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604993"
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
  

