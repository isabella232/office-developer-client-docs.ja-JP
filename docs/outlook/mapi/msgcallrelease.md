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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801647"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**適用対象**: Outlook 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数を使用してその上に構築された**IMessage**オブジェクトの最終的なリリース後**IStorage**インターフェイスを解放するコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装される関数の定義:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>パラメーター

 _ulCallerData_
  
> [in]**IMessage**インターフェイスの呼び出し元のアプリケーションの情報が含まれています。 
    
 _lpMessage_
  
> [in]最上位のメッセージおよびリリースされた添付ファイルへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  

