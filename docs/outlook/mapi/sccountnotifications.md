---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437995"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知の配列のサイズをバイト単位で指定し、配列に関連付けられているメモリを検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cntf_
  
> 順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。 
    
 _rgntf_
  
> 順番サイズが決定される**通知**構造の配列へのポインター。 
    
 _設計_
  
> 読み上げ(オプション) _rgntf_パラメーターで指定された配列のサイズ (バイト単位) を指すポインターです。 NULL の場合、 **sccountnotifications**は通知の配列を検証します。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> カウントが正常に決定されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

_pcb_パラメーターで NULL が渡された場合、 **sccountnotifications**関数は通知の配列のみを検証しますが、カウントは行われません。非 null 値が_pcb_で渡された場合、 **sccountnotifications**は配列のサイズを決定し、原因となった_pcb_を格納します。 _pcb_パラメーターは、配列全体を格納するのに十分な大きさである必要があります。 
  

