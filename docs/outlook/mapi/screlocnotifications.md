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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803863"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

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
    
## <a name="remarks"></a>備考

_Pcb_ **ScRelocNotifications**関数のパラメーターはオプションです。 
  
## <a name="see-also"></a>関連項目



[ScRelocProps](screlocprops.md)

