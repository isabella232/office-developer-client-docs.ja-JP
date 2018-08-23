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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573188"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  

