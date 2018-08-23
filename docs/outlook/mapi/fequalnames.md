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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570850"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
2 つの MAPI 名前付きプロパティが同じかどうかを判断します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>パラメーター

 _lpName1_
  
> [in]最初の名前付きプロパティを記述する[MAPINAMEID](mapinameid.md)構造体へのポインター。 
    
 _lpName2_
  
> [in]2 番目の名前付きプロパティを記述する**MAPINAMEID**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 2 つのプロパティ名は、同じです。 
    
FALSE 
  
> 2 つのプロパティ名が等しくないです。
    
## <a name="remarks"></a>注釈

**FEqualNames**関数は、 **MAPINAMEID**構造体は[GUID](guid.md)が含まれていて、複数の方法でプロパティ名自体を表すことができますので便利です。 つまり、バイナリの簡単な方法で 2 つの構造体を比較することはできません。 
  
テスト プロセスは、プロパティ名の文字列の大文字小文字を区別します。 
  

