---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412038"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ セッションと、そのセッション内で作成されたすべてのメッセージを閉じます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpMsgSess_
  
> [in]メッセージ セッションの最初に [OpenIMsgSession](openimsgsession.md) 関数を使用して取得したメッセージ セッション オブジェクトへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

メッセージ セッションは、基になる OLE **IStorage** オブジェクトの上に構築された複数の関連する MAPI **IMessage** オブジェクトを処理するクライアント アプリケーションおよびサービス プロバイダーによって使用されます。 クライアントまたはプロバイダーは [、OpenIMsgSession](openimsgsession.md) 関数と **CloseIMsgSession** 関数を使用して、メッセージ セッション内でこのようなメッセージの作成をラップします。 メッセージ セッションを開いた後、クライアントまたはプロバイダーは [OpenIMsgOnIStg](openimsgonistg.md) への呼び出しでポインターを渡して、新しい **IMessage**-on- **IStorage** オブジェクトを作成します。 
  
メッセージ セッションでは、すべての添付ファイルとメッセージの他のプロパティに加えて、セッション期間中に開いたすべての **IMessage**-on- **IStorage** オブジェクトが追跡されます。 クライアントまたはプロバイダーが **CloseIMsgSession** を呼び出す場合、これらのオブジェクトはすべて閉じます。 **CloseIMsgSession** を呼び出す方法は **、IMessage**-on- **IStorage オブジェクトを閉じる唯一の方法** です。 
  

