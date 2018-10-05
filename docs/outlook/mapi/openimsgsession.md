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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389625"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
作成し、その中に作成されたメッセージをグループ化するメッセージ セッションを開きます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpMalloc_
  
> [in]OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 MAPI では、OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)インターフェイスを使用する場合、この割り当てメソッドを使用する必要があります。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lppMsgSess_
  
> [out]返されるメッセージのセッション オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> セッションが開かれました。
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_または_lppMsgSess_は、NULL です。 
    
MAPI_E_INVALID_FLAGS
  
> 無効なフラグが渡されました。
    
MAPI_UNICODE
  
> この関数を呼び出す場合、クライアントまたはサービス プロバイダーは、Unicode の .msg ファイルを作成するのには MAPI_UNICODE フラグを設定します。 [Imessage](imessageimapiprop.md)ファイルでは、その PR_STORE_SUPPORT_MASK に STORE_UNICODE_OK を示しています、Unicode プロパティをサポートしています。 
    
## <a name="remarks"></a>備考

メッセージ セッションがクライアント アプリケーションによって使用され、いくつかに対処するために必要なサービス プロバイダーに関連する MAPI [IMessage: IMAPIProp](imessageimapiprop.md)オブジェクトの基になる OLE **IStorage**オブジェクトの上に構築します。 クライアントまたはプロバイダーは、 **OpenIMsgSession**と[CloseIMsgSession](closeimsgsession.md)関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。 メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。 
  
メッセージ セッションの追跡 - 点灯 - **IStorage**オブジェクトのすべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に作成されたすべての**IMessage**です。 クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。 -点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。 
  
 **OpenIMsgSession**は、クライアントと OLE **IStorage**オブジェクトに関連するいくつかのメッセージを処理する能力を必要とするプロバイダーが使用されます。 だけこのような 1 つのメッセージを同時に開くことが、複数のメッセージと**OpenIMsgSession**とメッセージ セッションを作成する理由を追跡する必要はありません。 
  
基になる OLE オブジェクトを扱うことはため、MAPI は、OLE のメモリの割り当てを使用する必要があります。 OLE 構造化ストレージ オブジェクトと OLE のメモリの割り当ての詳細については、 [OLE アプリケーションとデータの転送](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。 
  

