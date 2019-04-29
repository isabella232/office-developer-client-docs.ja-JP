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
  
2つの MAPI 名前付きプロパティが同じかどうかを判断します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>パラメーター

 _lpName1_
  
> 順番最初の名前付きプロパティを説明する[mapinameid](mapinameid.md)構造体へのポインター。 
    
 _lpName2_
  
> 順番2番目の名前付きプロパティを説明する**mapinameid**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 2つのプロパティ名は同じです。 
    
FALSE 
  
> 2つのプロパティ名は同じではありません。
    
## <a name="remarks"></a>注釈

**mapinameid**構造には[GUID](guid.md)が含まれ、プロパティ名自体を複数の方法で表すことができるので、 **FEqualNames**関数は便利です。 これは、2つの構造体を単純な binary メソッドと比較できないことを意味します。 
  
テストプロセスでは、プロパティ名文字列の大文字と小文字が区別されます。 
  

