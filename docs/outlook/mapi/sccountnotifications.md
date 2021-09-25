---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de46b401053fa31b93d1dbd2f34a1741a8da1a1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578712"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知の配列のサイズ (バイト単位) を決定し、配列に関連付けられているメモリを検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cntf_
  
> [in]_rgntf_[パラメーターで](notification.md)示される配列内の NOTIFICATION 構造体の数。 
    
 _rgntf_
  
> [in]サイズを決定する **NOTIFICATION** 構造体の配列へのポインター。 
    
 _pcb_
  
> [out]  _rgntf_ パラメーターが指す配列のサイズ (バイト単位) へのオプションのポインター。 NULL の場合 **、ScCountNotifications は** 通知の配列を検証します。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> カウントが正常に決定されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

_NULL_ が pcb パラメーターで渡された場合 **、ScCountNotifications** 関数は通知の配列のみを検証しますが、カウントは行われます。null 以外の値が _pcb_ で渡された場合 **、ScCountNotifications は** 配列のサイズを決定し、原因 _の pcb_ を格納します。 pcb  _パラメーターは_ 、配列全体を格納するのに十分な大きい値である必要があります。 
  

