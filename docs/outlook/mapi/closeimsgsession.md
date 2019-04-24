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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334938"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージセッションと、そのセッション内で作成されたすべてのメッセージを閉じます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpmsgsess_
  
> 順番メッセージセッションの開始時に[OpenIMsgSession](openimsgsession.md)関数を使用して取得したメッセージセッションオブジェクトへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

メッセージセッションは、基になる OLE **IStorage**オブジェクトの上に構築された複数の関連する MAPI **IMessage**オブジェクトを処理するクライアントアプリケーションおよびサービスプロバイダーによって使用されます。 クライアントまたはプロバイダーは、 [OpenIMsgSession](openimsgsession.md)関数と**CloseIMsgSession**関数を使用して、メッセージセッション内のメッセージの作成をラップします。 メッセージセッションが開かれると、クライアントまたはプロバイダーは、 [OpenIMsgOnIStg](openimsgonistg.md)への呼び出しによって、新しい**IMessage**オブジェクトを作成するために**** ポインターを渡します。 
  
メッセージセッションは、メッセージのすべての添付ファイルと**** その他のプロパティに加えて、セッションの間に開かれたすべての**IMessage**オブジェクトを追跡します。 クライアントまたはプロバイダーが**CloseIMsgSession**を呼び出すと、これらのすべてのオブジェクトが閉じられます。 **CloseIMsgSession**の呼び出しは、 **IMessage**で、 **IStorage**オブジェクトを閉じる唯一の方法です。 
  

