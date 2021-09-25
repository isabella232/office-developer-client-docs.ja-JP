---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 648a47a814071911aafad9f1b091a47a2647cc66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595659"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数を使用して、その上に構築された **IMessage** オブジェクトの最終リリース後に **IStorage** インターフェイスを解放できるコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>パラメーター

 _ulCallerData_
  
> [in]IMessage インターフェイスに関する呼び出し元 **のアプリケーション情報が含** まれる。 
    
 _lpMessage_
  
> [in]リリースされたトップ レベルのメッセージと添付ファイルへのポインター。
    
## <a name="return-value"></a>Return value

なし。
  

