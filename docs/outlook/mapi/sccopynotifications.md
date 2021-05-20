---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435923"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知のグループを 1 つのメモリ ブロックにコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cntf_
  
> [in]_rgntf_[パラメーターで](notification.md)示される配列内の NOTIFICATION 構造体の数。 
    
 _rgntf_
  
> [in]コピーするイベント **通知を** 定義する NOTIFICATION 構造体の配列へのポインター。 
    
 _pvDst_
  
> [out]返される通知へのポインター。 
    
 _pcb_
  
> [out]  _rgntf_ パラメーターが指す配列のサイズ (バイト単位) が格納される変数へのオプションのポインター。 NULL 以外の場合  _、pcb_ パラメーターは  _pvDst_ パラメーターに格納されているバイト数に設定されます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> イベント通知が正常にコピーされました。
    
E_INVALIDARG
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

NULL が pcb パラメーター  _で渡された_ 場合、コピーは実行されません。null 以外の値が  _pcb_ で渡された場合 **、ScCopyNotifications** 関数は配列と配列自体のサイズを 1 つのメモリ ブロックにコピーします。 _pcb が_ NULL ではない場合、pvDst パラメーターに格納されているバイト数 _に設定_ されます。 _pvDst パラメーターは_、配列全体を含むのに十分な大きい値である必要があります。 
  

