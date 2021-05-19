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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415202"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したイベント通知配列内のポインターを調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]_rgntf_[パラメーターで](notification.md)示される配列内の NOTIFICATION 構造体の数。 
    
 _rgntf_
  
> [in]ポインターを調整するイベント **通知** を定義する NOTIFICATION 構造体の配列へのポインター。 
    
 _pvBaseOld_
  
> [in]  _rgntf_ パラメーターで示される配列の元のベース アドレスへのポインター。 
    
 _pvBaseNew_
  
> [in] **ScRelocNotifications** が  _rgntf_ パラメーターで示す配列の新しい基本アドレスを書き込む場所。 
    
 _pcb_
  
> [out]  _pvBaseNew_ パラメーターで示される配列のサイズ (バイト単位) へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

**ScRelocNotifications** 関数の pcb パラメーターはオプションです。  
  
## <a name="see-also"></a>関連項目



[ScRelocProps](screlocprops.md)

