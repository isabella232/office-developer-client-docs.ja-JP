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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803837"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**適用されます**: Outlook 
  
イベント通知では、配列のバイト単位のサイズを決定し、配列に関連付けられているメモリを確認します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cntf_
  
> [in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。 
    
 _rgntf_
  
> [in]サイズを確認する**通知**の構造体の配列へのポインター。 
    
 _pcb_
  
> [out]ポインターを_rgntf_パラメーターが指す配列のバイト単位のサイズを指します。 NULL の場合、 **ScCountNotifications**は、通知の配列を検証します。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> カウントが正常に確認されました。
    
MAPI_E_INVALID_PARAMETER
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>備考

_Pcb_のパラメーターに NULL が渡されると、 **ScCountNotifications**関数は、さまざまな通知だけを検証が、カウントは行われません。**ScCountNotifications**が配列のサイズを決定し、原因を格納する_pcb_の null 以外の値が渡された場合_pcb_です。 _Pcb_のパラメーターは、配列全体を格納できる大きさである必要があります。 
  

