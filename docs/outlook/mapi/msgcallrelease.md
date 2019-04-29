---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405913"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数を使用して、その上に構築された**IMessage**オブジェクトの最終リリース後に、 **IStorage**インターフェイスを解放できるコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|定義された関数の実装:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>パラメーター

 _ulcallerdata_
  
> 順番**IMessage**インターフェイスに関する通話アプリケーション情報が保存されています。 
    
 _lpmessage_
  
> 順番最上位レベルのメッセージと、解放された添付ファイルへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  

