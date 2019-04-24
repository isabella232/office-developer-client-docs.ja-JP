---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299546"
---
# <a name="getinstance"></a>GetInstance

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数値プロパティ内の1つの値を、同じ型の単一値プロパティにコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |MAPIUTIL。H  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>パラメーター

 _pvalmv_
  
> 順番複数値プロパティを定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
 _pvalsv_
  
> 順番データを受け取る単一値プロパティへのポインター。 
    
 _uliInst_
  
> 順番_pvalmv_パラメーターで指定された構造体からコピーされる値のインスタンス番号 (array 要素)。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

コピーされた値が割り当てられたメモリに対して大きすぎる場合、 **GetInstance**関数は新しいメモリを割り当てる代わりにポインターのみをコピーします。 
  

