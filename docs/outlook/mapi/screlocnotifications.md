---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360712"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定されたイベント通知配列内のポインターを調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cntf_
  
> 順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。 
    
 _rgntf_
  
> 順番ポインターが調整される必要のあるイベント通知を定義する**通知**構造の配列へのポインター。 
    
 _pvbaseold_
  
> 順番_rgntf_パラメーターで指定された配列の元のベースアドレスへのポインター。 
    
 _pvBaseNew_
  
> 順番**ScRelocNotifications**が_rgntf_パラメーターで指定された配列の新しいベースアドレスを書き込む場所。 
    
 _設計_
  
> 読み上げ_pvBaseNew_パラメーターで指定された配列のサイズ (バイト単位) へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>解説

**ScRelocNotifications**関数の_pcb_パラメーターは省略可能です。 
  
## <a name="see-also"></a>関連項目



[ScRelocProps](screlocprops.md)

