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
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583968"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
指定したイベント通知の配列内のポインターを調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。 
    
 _rgntf_
  
> [in]ポインターを調整するのには、イベント通知を定義する**通知**の構造体の配列へのポインター。 
    
 _pvBaseOld_
  
> [in]_Rgntf_パラメーターで指定された配列の元のベース アドレスへのポインター。 
    
 _pvBaseNew_
  
> [in]**ScRelocNotifications**の_rgntf_パラメーターで指定された配列の新しいベース アドレスの書き込み先の場所。 
    
 _pcb_
  
> [out]_PvBaseNew_パラメーターで指定された配列のバイト単位のサイズへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

_Pcb_ **ScRelocNotifications**関数のパラメーターはオプションです。 
  
## <a name="see-also"></a>関連項目



[ScRelocProps](screlocprops.md)

