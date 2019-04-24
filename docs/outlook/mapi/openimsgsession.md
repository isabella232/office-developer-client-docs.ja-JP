---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326195"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
その中で作成されたメッセージをグループ化するメッセージセッションを作成して開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpmalloc_
  
> 順番OLE [imalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 MAPI は、OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)インターフェイスで作業するときに、この割り当て方法を使用する必要があります。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lppmsgsess_
  
> 読み上げ返されたメッセージセッションオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> セッションが開かれました。
    
MAPI_E_INVALID_PARAMETER
  
>  _lpmalloc_または_lppmsgsess_ NULL です。 
    
MAPI_E_INVALID_FLAGS
  
> 無効なフラグが渡されました。
    
MAPI_UNICODE
  
> この関数を呼び出すと、クライアントまたはサービスプロバイダーは、MAPI_UNICODE フラグを設定して、UNICODE の .msg ファイルを作成します。 生成された[Imessage](imessageimapiprop.md)ファイルは、PR_STORE_SUPPORT_MASK に STORE_UNICODE_OK を表示し、UNICODE プロパティをサポートします。 
    
## <a name="remarks"></a>解説

メッセージセッションは、基になる OLE **IStorage**オブジェクトの上に構築された複数の関連する MAPI [IMessage: imapiprop](imessageimapiprop.md)オブジェクトを処理するクライアントアプリケーションおよびサービスプロバイダーによって使用されます。 クライアントまたはプロバイダーは、 **OpenIMsgSession**関数と[CloseIMsgSession](closeimsgsession.md)関数を使用して、メッセージセッション内のメッセージの作成をラップします。 メッセージセッションが開かれると、クライアントまたはプロバイダーは、 [OpenIMsgOnIStg](openimsgonistg.md)への呼び出しによって、新しい**IMessage**オブジェクトを作成するために**** ポインターを渡します。 
  
メッセージセッションは、メッセージのすべての添付ファイルと**** その他のプロパティに加えて、セッションの期間中に作成されたすべての**IMessage**オブジェクトを追跡します。 クライアントまたはプロバイダーが**CloseIMsgSession**を呼び出すと、これらのすべてのオブジェクトが閉じられます。 **CloseIMsgSession**の呼び出しは、 **IMessage**で、 **IStorage**オブジェクトを閉じる唯一の方法です。 
  
 **OpenIMsgSession**は、複数の関連するメッセージを OLE **IStorage**オブジェクトとして処理する機能を必要とするクライアントとプロバイダーによって使用されます。 そのようなメッセージを一度に1つだけ開く場合は、複数のメッセージを追跡する必要がなく、 **OpenIMsgSession**を使用してメッセージセッションを作成する理由もありません。 
  
基になる ole オブジェクトを処理しているため、MAPI は ole メモリ割り当てを使用する必要があります。 ole 構造化ストレージオブジェクトと ole メモリ割り当ての詳細については、「 [ole とデータ転送](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)」を参照してください。 
  

