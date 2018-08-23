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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803811"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**適用対象**: Outlook 
  
イベント通知のグループを単一のメモリ ブロックにコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。 
    
 _rgntf_
  
> [in]コピーするイベント通知を定義する**通知**の構造体の配列へのポインター。 
    
 _pvDst_
  
> [out]返された通知へのポインター。 
    
 _pcb_
  
> [out]変数配列のバイト単位のサイズが_rgntf_パラメーターが指す場所にポインターが格納されます。 かどうか NULL の場合、 _pcb_のパラメーターは、 _pvDst_パラメーターに格納されているバイト数を設定します。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> イベント通知が正常にコピーされました。
    
E_INVALIDARG
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>注釈

_Pcb_のパラメーターに NULL を渡した場合は、コピーは実行されません。_pcb_の null 以外の値が渡された場合、 **ScCopyNotifications**関数は、単一ブロックのメモリをアレイとアレイ自体のサイズをコピーします。 _Pcb_が NULL でない場合は、 _pvDst_パラメーターに格納されているバイト数に設定されています。 _PvDst_パラメーターは、配列全体を格納できる大きさである必要があります。 
  

